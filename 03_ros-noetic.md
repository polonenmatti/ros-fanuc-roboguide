In this section we explain installation of ros-noetic on WSL2 Ubuntu 20.04 following [Source: ROS Wiki Single Line installation](http://wiki.ros.org/ROS/Installation/TwoLineInstall/)

In ubuntu 20.04 terminal type:

`wget -c https://raw.githubusercontent.com/qboticslabs/ros_install_noetic/master/ros_install_noetic.sh && chmod +x ./ros_install_noetic.sh && ./ros_install_noetic.sh`

It's going to ask your SUDO password that you created on first start up.

Next it ask what kind of ros install you want to do. Choose 1. Desktop-Full Install.

After that run:

`rosdep update --include-eol-distros`

Open new terminal, start ubuntu2004.exe and run:

`rosversion -d`

You should get:

<img width="308" height="91" alt="image" src="https://github.com/user-attachments/assets/866370fd-dd6d-43c7-9001-84ee31404fe0" />



