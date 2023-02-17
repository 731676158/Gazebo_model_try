安装一些没有提到的依赖
sudo apt-get install ros-melodic-serial ros-melodic-move-base
sudo apt-get install ros-melodic-teleop-twist-keyboard

如果出现libcurl问题
sudo gedit ~/.ignition/fuel/config.yaml
把api.ignitionfuel.org改称api.ignitionrobotics.org

如果gazebo没有响应
gazebo --verbose
如果报错的话
killall gzserver
killall gzclient

