Luan Van Thac Si
1.Thay đổi Architecture Yolov5
Proposed model
 
Code change:
1.Model
Vị trí : yolov5/models/yolov5s.yaml(có thể chọn các version khác)

 

2 . Lớp ECAC3
a.Vị trí : yolov5/models/common.py
-Add class eca_layer(nn.Module):
        class ECAC3(nn.Module):
b.Vi trí : yolov5/models/yolo.py
-Add ECAC3 vào array

3.Lớp GAM 
a.Vị trí : yolov5/models/common.py
-Add class GAM_Attention(nn.Module)
b.Vi trí : yolov5/models/yolo.py
-Thêm lớp atte

4.Thêm hàm h-swish , shuffle
Vị trí yolov5/models/common.py
Add class h_swish , class h_sigmoid and def channel_shuffle
