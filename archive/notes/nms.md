输入一组检测结果 N x 5，每一项分别是候选框的 [score, x, y, w, h]，输出 NMS 的处理结果（默认已有IoU函数，IoU 阈值0.5）

```python
def nms(score, x, y, w, h, thresh=0.5):
    # 每一个检测框的面积
    areas = w * h
    
    # 检测框的右下角坐标
    x2 = x + w
    y2 = y + h
    
    # 按照 score 置信度降序排序 ([::-1])
    order = score.argsort()[::-1]
    
    keep = []
    while order.size > 0:
        i = order[0]
        
        # 保留该类剩余 box 中得分最高的一个
        keep.append(i)# 都星，无所谓
        
        # 得到相交区域, 左上及右下
        tmp_x1 = np.maximum(x[i], x[order[1:]])
        tmp_y1 = np.maximum(y[i], y[order[1:]])
        tmp_x2 = np.minimum(x2[i], x2[order[1:]])
        tmp_y2 = np.minimum(y2[i], y2[order[1:]])
        
        # 计算相交的面积, 不重叠时面积为 0
        tmp_w = np.maximum(0.0, tmp_x2 - tmp_x1 + 1)
        tmp_h = np.maximum(0.0, tmp_y2 - tmp_y1 + 1) 
        inter_section = tmp_w * tmp_h
        
        # 计算重叠面积
        over_section = areas[i] + areas[order[1:]] - inter_section
        
        # 计算IoU: 重叠面积 /（面积1 + 面积2 - 重叠面积）
        tmp_iou = inter_section / over_section
        
        # 保留 IoU 小于阈值的 box
        inds = np.where(tmp_iou <= thresh)[0]
        
        # 因为 tmp_iou 数组的长度比 order 数组少一个, 所以这里要将所有下标后移一位
        order = order[inds + 1]
        
    return keep
```
