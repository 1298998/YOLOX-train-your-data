# YOLOX train your data

you need generate data.txt like follow format **(per line-> one image)**.

## **prepare one data.txt like this:**

img_path1 x1,y1,x2,y2,class_id x1,y1,x2,y2,class_id2img_path2 x1,y1,x2,y2,class_idimg_path3 ..........

### **note:**

**x1,y1,x2,y2 is int type and it belong to 0-img_w ,0-img_h, not 0~1 !!!**

**img_path is abs path ;must be careful the sign " " and "," in data.txt**

**there was an example:/home/sal/images/000010.jpg 0,190,466,516,1/home/sal/images/000011.jpg 284,548,458,851,7 256,393,369,608,1**

## **Train**

### i. step1 , before train, you need change yolox/exp/yolox_base.py follow you need, i add some explain in it.

- from yolox.exp.base_exp import BaseExp<br>
1.  num_classes
2. train_txt
3. val_txt

### ii. step2 , change train.py params, just as https://github.com/Megvii-BaseDetection/YOLOX.git ,when you have changed , just run : **python train.py**

### **iii. star****