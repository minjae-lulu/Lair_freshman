
# segmentation_ros

## how to build

```
cd ~/catkin_ws/src
git clone https://github.com/thithin-ent/segmentation_ros.git
cd ..
catkin_make
source ~/catkin_ws/devel/setup.bash
```

## how to use

```
roslaunch segmentation_ros run.launch
```


데이터 kitti 썼으며, src 폴더안의 segmentation_ros.cpp 파일의 9번째줄이 kitti dataset 경로설정한것이다. 나는 aloam 돌릴때 키티 데이터셋을 받아서 경로를 아래처럼 설정해준것이다. 나중에 데이터셋 위치에따라 수정해주어야 한다. <br>

dataset_folder_ = "/home/user/Desktop/aloam-tutorial/data/dataset/";
