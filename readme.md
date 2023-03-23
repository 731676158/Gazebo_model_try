安装一些没有提到的依赖
sudo apt-get install ros-melodic-serial ros-melodic-move-base ros-melodic-gmapping ros-melodic-hector-gazebo-plugins
sudo apt-get install ros-melodic-teleop-twist-keyboard ros-melodic-amcl ros-melodic-map-server ros-melodic-joint-state-publisher-gui


如果出现libcurl问题
sudo gedit ~/.ignition/fuel/config.yaml
把api.ignitionfuel.org改称api.ignitionrobotics.org

如果gazebo没有响应
gazebo --verbose
如果报错的话
killall gzserver
killall gzclient

如果what():  boost::filesystem::status: 权限不够: ".gvfs" gazebo
sudo umount /home/useraccount/.gvfs
rm -rf .gvfs

控制小车命令：
ROS_NAMESPACE=vehicle_1 rosrun teleop_twist_keyboard teleop_twist_keyboard.py

标定：
[calib](https://blog.csdn.net/weixin_42141088/article/details/118000544)

报错：
“Traceback (most recent call last):
  File "/opt/ros/melodic/lib/gazebo_ros/spawn_model", line 239, in <module>
    exit_code = sm.run()
  File "/opt/ros/melodic/lib/gazebo_ros/spawn_model", line 149, in run
    xml_parsed = xml.etree.ElementTree.fromstring(model_xml)
  File "/usr/lib/python2.7/xml/etree/ElementTree.py", line 1311, in XML
    parser.feed(text)
  File "/usr/lib/python2.7/xml/etree/ElementTree.py", line 1657, in feed
    self._parser.Parse(data, 0)
UnicodeEncodeError: 'ascii' codec can't encode character u'\u5b8f' in position 492: ordinal not in range(128)”

[link](https://blog.csdn.net/kylinnirvana/article/details/119516684)
