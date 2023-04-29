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

ros2 launch vacuum_bot launch_sim.launch.py
```

If you now open RViz you should see the robot.

_Note : It's possible that Gazebo can't find models. In this case, copy models' folder to `vacuum_ws/install/vacuum_bot/share/vacuum_bot/models` :_

```bash
cp -r models ~/vacuum_ws/install/vacuum_bot/share/vacuum_bot
```

_Note 2 : Gazebo is experiencing some weird issues. If you get this error : `gzclient: /usr/include/boost/smart_ptr/shared_ptr.hpp:734:typename boost::detail::sp_member_access<T>::type boost::shared_ptr<T>::operator->() const [with T = gazebo::rendering::Camera; typename boost::detail::sp_member_access<T>::type gazebo::rendering::Camera*]: Assertion 'px != 0' failed.`, you should `source /usr/share/gazebo/setup.sh`._

## Playing
Since you have launched the simulation you could control the robot by launching teleop : `ros2 run teleop_twist_keyboard teleop_twist_keyboard`.