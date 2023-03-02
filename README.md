# GRADE_data
This repository contains all the data related to the GRADE project.

For each download we provide the link and a brief description. 

### Training/validation data --- COCO and YOLO formats
1. TUM RGBD walking sequences labelled [yolo](https://keeper.mpdl.mpg.de/f/5346f793e0c7402a957c/) and [mrcnn](https://keeper.mpdl.mpg.de/f/240fce3f4ca24dc4a1f4/) formats.
   To keep things simple in `mrcnn` you have a `val2017` with all the images and a `annotations/instances_val2017.json` with all the annotations in COCO format. Thus, you can simply use a coco loader with this json/folder to load the data. 
   The `yolo` simply contains the `images` and `labels` folder.
   You can find the online version in [roboflow](https://universe.roboflow.com/tum-osduz/tum-fr3-walking)
2. [S-GRADE](https://keeper.mpdl.mpg.de/f/19ce92e2c7b048219b2a/), small subset of the GRADE dataset. You can find the jsons in COCO format for the masks, all the labels in yolo format, and both the groundtruth and the noisy images.

3. [S-COCO](https://keeper.mpdl.mpg.de/f/fc09f2f6afc640f3b3bf/), small subset of COCO dataset. You can find the jsons in COCO format for the masks, all the labels in yolo format, and the images.

### Trained models
[YOLO](https://keeper.mpdl.mpg.de/f/88a56a9325114bb6b37c/)

[MRCNN](https://keeper.mpdl.mpg.de/f/9bbfefa5d68d433b99e5/)

The npy files with the evaluation results of mrcnn are [here](https://keeper.mpdl.mpg.de/f/0a2b913f51514616a313/). For YOLO you can easily do these given the data above. 

The list of results using these trained models with DynaSLAM and DynamicVINS are [here](https://keeper.mpdl.mpg.de/f/0a2b913f51514616a313/).

### SLAM tested sequences
For each we provide the original groundtruth rosbags and the noisy ones. Most of the folders have the logs/rosbags from which we extracted the results you can find in the paper.

1. [F](https://keeper.mpdl.mpg.de/f/37a0dc5a855547b5b892/) With few flying objects
2. [FH](https://keeper.mpdl.mpg.de/f/f479032ed14e4244a814/) With few flying objects, horizontal
3. [D](https://keeper.mpdl.mpg.de/f/de3f917c925d46a9b39f/) Dynamic without flying objects
4. [DH](https://keeper.mpdl.mpg.de/f/6a23acba9dba40a4865a/) Dynamic without flying objects, horizontal
5. [WO](https://keeper.mpdl.mpg.de/f/1d6dfb859dcb4ac69be9/)  With occlusions
6. [WOH](https://keeper.mpdl.mpg.de/f/a6d613c780344b5393df/) With occlusion, horizontal
7. [S](https://keeper.mpdl.mpg.de/f/f65c55ae0c0b4e8ebb90/) Static
8. [SH](https://keeper.mpdl.mpg.de/f/e49efeb92414482ba478/) Static, horizontal

The complete list of results, including RPE and ATE are [here]().

For licensing information, please refer to the main repository located [here](https://github.com/eliabntt/GRADE-RR/).
