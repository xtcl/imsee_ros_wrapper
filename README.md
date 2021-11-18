# imsee_ros_wrapper
ros_wrapper for indemind

# install
```bash
$ cd ros_ws
$ mkdir -p devel/lib/imsee_ros_wrapper
$ ./src/imsee_ros_wrapper/scripts/init.sh
$ ./src/imsee_ros_wrapper/scripts/cp_files_ros.sh
$ catkin_make -DCMAKE_BUILD_TYPE=$(BUILD_TYPE)
```

# run
```bash
$ sudo su #开启权限模式
$ source devel/setup.bash
$ roslaunch imsee_ros_wrapper start.launch
```

# calib
```bash
rosrun camera_calibration cameracalibrator.py --approximate 0.1 --size 8x6 --square 0.02585 --no-service-check right:=/imsee/image/right left:=/imsee/image/left
```
