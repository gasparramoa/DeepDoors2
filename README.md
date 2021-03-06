# DeepDoors2  Dataset  [:door:]
DeepDoors2 is a dataset for 2D/3D door classification, 2D door detection and 2D door segmentation. <br/> <br/>
The images were obtained using a 3D Realsense Camera, model D435. The camera was rotated 90 degrees since its horizontal viewing angle(86 degrees) is bigger than its vertical viewing angle(57 degrees) with the purpose of including all the door area in the images.
The images captured are from Universidade da Beira Interior, public places and people's houses with several doors and its surroundings with different textures and sizes. This Dataset is divided in two sub-datasets, one for door detection/semantic segmentation with 3000 images and the other for door classification also with 3000 images. \
Further details of the sub-datasets are described below.


## DeepDoors2 Detection | SemanticSegmentation
This subdataset has a total of 3000 RGB images with the size 480 x 640. The pixel value of the images is 192,224,192 if it corresponds to a door or door frame, and is 0,0,0 if it does not (background). 

![Samples for door detection dataset](doors2.jpg)

## DeepDoors2 Classification [3D and RGB]
This subdataset has a total of 3000 RGB door images and the 3000 corresponded depth images.
Both with the size 480 x 640 pixels. The depth images are in grey-scale with pixels values between 0 and 255 and the depth scale used was equal to 1/16. The depth in meters is equal to depth scale * pixel value, for example, if the pixel value is equal to 32 it means that that pixel is 2 meters away from the viewer(1/16 * 32 = 2). 
The dataset has 1000 closed door images, 1000 open door images and 1000 semi-open doors images. It is also divided in test, validation and train set. For the validation and test set it were used 100 samples of each class giving a total of 300 samples for test and 300 samples for validation. The remaning samples were used to built the training set (2400 images).

![Samples for door classification dataset](doors1.jpg)

## Link to dataset
Link [here](https://drive.google.com/drive/folders/1SxVKeJ9RBcoJXHSHw-LWaLGG07BZT-b5?usp=sharing)


## Intrinsic matrix (pixels)
width: 640, height: 480 \
ppx(cx): 319.226, ppy(cy): 242.138, fx: 384.681, fy:384.681, s: 0


## Data Structure
DeepDoors2
* Door Detection|Segmentation
  * Annotations
  * Images

  
* Door Classification
  * Depth
    * Test
      * Closed
      * Open
      * Semi-open
    * Train
      * Closed
      * Open
      * Semi-open
    * Val
      * Closed
      * Open
      * Semi-open
  * RGB
    * Test
      * Closed
      * Open
      * Semi-open
    * Train
      * Closed
      * Open
      * Semi-open
    * Val
      * Closed
      * Open
      * Semi-open   
       
 ## Dataset Caracteristics
 
 The DeepDoors2 Dataset is the version 2.0 of [[Door Detection & Classification] Dataset](https://github.com/gasparramoa/DoorDetect-Class-Dataset) with several improvements.
 * Obstacles in front of the doors (Tables, chairs, etc.).
 * Contains blurred images.
 * Doors with glass.
 * Double doors.
 * Outdoor doors.
 * People and animals in front of the doors.
 
       
 ## Acknowledgments      
       
 To Nuno, Bruno, Vasco, Diogo, Simão.      
       
 ## Citation :page_with_curl:
 If you use this dataset, please cite:
```
@article{article,
author = {Ramôa, João and Lopes, Vasco and Alexandre, Luís and Mogo, Sandra},
year = {2021},
month = {05},
pages = {},
title = {Real-time 2D–3D door detection and state classification on a low-power device},
volume = {3},
journal = {SN Applied Sciences},
doi = {10.1007/s42452-021-04588-3}
}
```


