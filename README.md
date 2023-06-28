Luan Van Thac Si
<space><space>

1.Thay đổi Architecture Yolov5
<space><space>

Proposed model
 <space><space>
 
Code change:
<space><space>

1.Model
<space><space>
Vị trí : yolov5/models/yolov5s.yaml(có thể chọn các version khác)
<space><space>
 

2 . Lớp ECAC3
<space><space>
a.Vị trí : yolov5/models/common.py
<space><space>
-Add class eca_layer(nn.Module):
<space><space>
        class ECAC3(nn.Module):
 <space><space>
b.Vi trí : yolov5/models/yolo.py
<space><space>
-Add ECAC3 vào array
<space><space>
3.Lớp GAM 
<space><space>
a.Vị trí : yolov5/models/common.py
<space><space>
-Add class GAM_Attention(nn.Module)
<space><space>
b.Vi trí : yolov5/models/yolo.py
<space><space>
-Thêm lớp atte
<space><space>
4.Thêm hàm h-swish , shuffle
<space><space>
Vị trí yolov5/models/common.py
<space><space>
Add class h_swish , class h_sigmoid and def channel_shuffle
