# Vacuum Bot

## Purpose of this software
This ROS2 Foxy package is used to convert a random vacuum robot into an over-engineered futuristic vacuum robot.

## Disclaimer
This project is under developpement and may change according to my ideas.

## Installation & Contribute
To run this package you will need ROS 2 Foxy installed on your system. You may clone this repo into your `src/` workspace's folder.

```bash
source /opt/ros/foxy/setup.bash

cd ~
mkdir -p vacuum_ws/src
cd vacuum_ws/src
git clone https://github.com/EG-Julien/vacuum_bot.git
cd ../
colcon build --symlink-install
source install/setup.bash

ros2 launch vacuum_bot rsp.launch.pyvac
```

If you now open RViz you should see the robot.