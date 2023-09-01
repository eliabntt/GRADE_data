# GRADE_data

## This repository is part of the [GRADE](https://eliabntt.github.io/GRADE-RR/home) project

For each download we provide the link and a brief description. 

We release data for:
1. [Indoor humans detection and segmentation](https://github.com/eliabntt/GRADE_data/#indoor-humans-detectionsegmentation)
2. [Static and Dynamic SLAM](https://github.com/eliabntt/GRADE_data/blob/main/README.md#slam-tested-sequences) sequences used in the GRADE paper
3. [Zebras](https://github.com/eliabntt/GRADE_data/blob/main/README.md#zebras) training data, synthetic data, animated USDs, and trained models
4. More data coming soon. This will include (as groundtruth, unless specified):
   1. Converted Front3D Environments
   2. Converted Cloth3D sequences
   3. Converted AMASS sequences
   4. Converted Google Scanned Objects
   5. Experiment USD files and informations
   6. Experiments RGB+DEPTH
   7. Experiments camera poses, robot poses, camera and robot IMU readings
   8. Experiments Instance segmentation
   9. Experiments bounding boxes and object poses
   10. Humans vertices, skeletal and 3D bbox information in world coordinate frame
   11. Re-indexed rosbags
________

## Indoor Humans Detection/Segmentation

### Training/validation data, COCO and YOLO formats, people segmentation/detection tasks
All the datasets can be found [here](https://keeper.mpdl.mpg.de/d/0b4869a60428479f8690/).

All the datasets have both the YOLO-style and the COCO-style labels. Converters between the two can be found in the [GRADE_tools](https://github.com/robot-perception-group/GRADE_tools) repository.

In there you will find:
1. TUM RGBD fr3/walking sequences labelled [link](https://keeper.mpdl.mpg.de/f/a3723c2c6b7d45c3bc7e/).
   You can find and improve the dataset in [roboflow](https://universe.roboflow.com/tum-osduz/tum-fr3-walking)
2. [S-GRADE](https://keeper.mpdl.mpg.de/f/b1400d9ee37f4faa8a97/), small subset of the GRADE dataset.
3. [S-COCO](https://keeper.mpdl.mpg.de/f/92c0bf21ddbe4531b40d/), small subset of COCO dataset containing only people. 
4. [A-GRADE](https://keeper.mpdl.mpg.de/f/8975b136ca7c470cb163/), full GRADE dataset.
5. [COCO](https://keeper.mpdl.mpg.de/f/e9ba574b614349898e9d/) the subset of COCO containing only people

### Trained models
[YOLOv5](https://keeper.mpdl.mpg.de/f/88a56a9325114bb6b37c/). Reproduce the results following using YOLOv5 at [this](https://github.com/ultralytics/yolov5/tree/5c91daeaecaeca709b8b6d13bd571d068fdbd003) commit.

[detectron2(i.e. MaskRCNN)]https://keeper.mpdl.mpg.de/f/9f4bc4a285c748c8bd45/). Reproduce the results following [this](https://github.com/robot-perception-group/GRADE_tools/tree/9cff9dbe7237da4fff93a26362369110e126c96e/mrcnn)

The results can be reproduced by using the networks at th
______

## Dynamic SLAM tested sequences

### GRADE data testing
For each we provide the original groundtruth rosbags and the noisy ones for both 3.5 and 5 meters depth. 

Following the paper convention we have
1. F - with few flying objects
2. FH - with few flying objects, horizontal
3. D - dynamic without flying objects
4. DH - dynamic without flying objects, horizontal
5. WO - with occlusions
6. WOH - with occlusion, horizontal
7. S - static
8. SH - static, horizontal

Note: the bag files are COMPRESSED. Run `rosbag decompress *.bag` in the desired folder to decompress them automatically. `rosbag info` will give you useful info on the contents of each bag.

You can find the rosbags in [this](https://keeper.mpdl.mpg.de/d/793782b63d6149cf88aa/) folder.

The complete list of results, including RPE and ATE can be found
1. [here](https://keeper.mpdl.mpg.de/f/79e79b6406f94d8980e5/) for the 3.5m bags
2. [here](https://keeper.mpdl.mpg.de/f/31e56cf0ca004bf6aec6/) for the 5m bags

The logs of the results will be published in the near future [todo](fillthis)

You can see how to process the rosbags to reproduce our results [here](https://github.com/robot-perception-group/GRADE_tools/tree/main)

### TUM RGBD walking sequences
The results using the network models trained above can be found [here](https://keeper.mpdl.mpg.de/f/4700b595ae444319bef8/). Please use our fork of [DynaSLAM](https://github.com/eliabntt/DynaSlam) when testing the `detectron2` models.

More information can be found [here](https://github.com/robot-perception-group/GRADE_tools/tree/main)

______

## Zebras

Please follow this [webpage](https://keeper.mpdl.mpg.de/d/12abb3bb6b12491480d5/). A readme will be inside.

_______

### LICENSING

For licensing information, please refer to the main repository located [here](https://github.com/eliabntt/GRADE-RR/).
__________

### CITATION

If you find this work useful please cite it based on [this](https://github.com/eliabntt/GRADE-RR#citation) information.
Please cite `GRADE` and `Synthetic Data-based Detection of Zebras in Drone Imagery` if you use any of the Zebra-related data.
Cite `GRADE` and the relative workshop paper if you use any code/data for dynamic SLAM/human detection projects.
