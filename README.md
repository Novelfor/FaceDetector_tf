# Tensorflow Face Detector
It's a ResNet50, [Faster R-CNN](https://arxiv.org/abs/1506.01497) based face detector. It include all steps for training a faster rcnn in a single jupyter notebook.

## Training on WIDER FACE Dataset.
The jupyter includes the code for preparing data from WIDER FACE datasets. Download the data from [WIDER FACE](http://mmlab.ie.cuhk.edu.hk/projects/WIDERFace/) and put them in data folder.

## Model details.
We train the model tranfered from the ImageNet pretrained ResNet50. The download code is in jupyter notebook.
Use the original image withou image resizing. And use some image augmentations to improve model performance.
Use learning rate decay. Use image resize instead of ROI Pooling, it's a common implementation of ROI Pooling in tensorflow. (It's different with the oral paper.)
Use [Joint Training](https://www.dropbox.com/s/xtr4yd4i5e0vw8g/iccv15_tutorial_training_rbg.pdf?dl=0) for ROI and RPN.

## Some Results.
![Examples](https://github.com/Novelfor/FaceDetector_tf/blob/master/imgs/example.png)

## Something else.
For Face Detection, R-CNN base method may not be a best way to implement it. MTCNN, Cascade CNN may be better.
No implementation of multiple GPUS. 
