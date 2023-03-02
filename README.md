# GRADE_data
This repository contains all the data related to the GRADE project.

For each download we provide the link and a brief description. 

### Training/validation data
1. TUM RGBD walking sequences labelled [yolo](https://keeper.mpdl.mpg.de/f/5346f793e0c7402a957c/) and [mrcnn](https://keeper.mpdl.mpg.de/f/240fce3f4ca24dc4a1f4/) formats.
   To keep things simple in `mrcnn` you have a `val2017` with all the images and a `annotations/instances_val2017.json` with all the annotations in COCO format. Thus, you can simply use a coco loader with this json/folder to load the data. 
   The `yolo` simply contains the `images` and `labels` folder.
   
2. [S-GRADE](), small subset of the GRADE dataset. You can find the jsons in COCO format for the masks, all the labels in yolo format, and both the groundtruth and the noisy images.
3. [S-COCO](https://keeper.mpdl.mpg.de/f/fc09f2f6afc640f3b3bf/), small subset of COCO dataset. You can find the jsons in COCO format for the masks, all the labels in yolo format, and the images.

### SLAM tested sequences
For each we provide the original groundtruth rosbags and the noisy ones. Most of the folders have the logs/rosbags from which we extracted the results you can find in the paper.

1. [F]()
2. [FH]()
3. [D]()
4. [DH]()
5. [WO]()
6. [WOH]()
7. [S]()
8. [SH]()

For licensing information please refer to the main repository located [here](https://github.com/eliabntt/GRADE-RR/).
