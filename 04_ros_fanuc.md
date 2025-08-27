In this section we install required fanuc driver packages on ROS stack.  [Following this](https://github.com/ros-industrial/fanuc)

Open terminal.
`sudo apt install ros-noetic-fanuc-m10ia-support`

Then we install movit
`sudo apt install ros-noetic-moveit`

We need to source couple things.

`echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc`
This makes sourcing automatic when opening new terminal.

`https://moveit.github.io/moveit_tutorials/doc/getting_started/getting_started.html#install-ros-and-catkin`

`rosdep update --include-eol-distros`
`sudo apt update`
`sudo apt dist-upgrade`

`sudo apt install ros-noetic-catkin python3-catkin-tools`
`sudo apt install python3-wstool`

`mkdir -p ~/ws_moveit/src`
`cd ~/ws_moveit/src`

`wstool init .`
`wstool merge -t . https://raw.githubusercontent.com/moveit/moveit/master/moveit.rosinstall`
`wstool remove moveit_tutorials  # this is cloned in the next section`
`wstool update -t .`

`cd ~/ws_moveit/src`
`git clone https://github.com/moveit/moveit_tutorials.git -b master`
`git clone https://github.com/moveit/panda_moveit_config.git -b noetic-devel`

`cd ~/ws_moveit/src`
`rosdep install -y --from-paths . --ignore-src --rosdistro noetic`

`sudo sh -c 'echo "deb http://packages.ros.org/ros-testing/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'`
`sudo apt update`

`cd ~/ws_moveit`
`catkin config --extend /opt/ros/${ROS_DISTRO} --cmake-args -DCMAKE_BUILD_TYPE=Release`
`catkin build`

`source ~/ws_moveit/devel/setup.bash`
`echo 'source ~/ws_moveit/devel/setup.bash' >> ~/.bashrc`

Terminal 1: 
`roscore`

Terminal 2:
`roslaunch panda_moveit_config demo.launch rviz_tutorial:=true`

From bottom bar:

<img width="508" height="500" alt="image" src="https://github.com/user-attachments/assets/e3e7909d-e7e3-46b1-ac56-506806613928" />

Add motion planning.

<img width="513" height="689" alt="image" src="https://github.com/user-attachments/assets/1eebafa1-cea0-42df-b7a8-c3eaa9be45fd" />



## Common issue 1

Rviz launches, but cannot see robot model after adding motion planning.

# Issue 1 - Possible solution 1

`sudo apt install mesa-utils`

Try to see this if your opengl rendering is working at all:

`glxgears`

Still might need to update mesa drivers to fresher and got to get ubuntu pro to get updates.


`sudo add-apt-repository ppa:kisak/kisak-mesa -y`

get it [www.ubuntu.com/pro](www.ubuntu.com/pro)

<img width="821" height="367" alt="image" src="https://github.com/user-attachments/assets/926f6ada-6cac-48fe-a2ef-7024238cc6d2" />

`sudo pro attach yourkeyhere`

`sudo apt upgrade`

This solution did not work for me.

# Issue 1 - Possible solution 2

Try [https://launchpad.net/~kisak/+archive/ubuntu/turtle/](https://launchpad.net/~kisak/+archive/ubuntu/turtle/)

`sudo add-apt-repository ppa:kisak/kisak-mesa`
`sudo apt update`

`glxinfo | grep "OpenGL version"`

OpenGL version string: 4.5 (Compatibility Profile) Mesa 25.0.7 - kisak-mesa PPA

After that try running again: 

Terminal 1: 

`roscore`

Terminal 2:

`roslaunch panda_moveit_config demo.launch rviz_tutorial:=true`

And add motion planning to rviz. This fixed issue for me.

# Common issue 2

After

`roslaunch panda_moveit_config demo.launch rviz_tutorial:=true`

terminal does not proceed. 

Try ctrl+c to close it. Sometimes it just runs after that. After starting once in terminal session, it usually starts again everytime.





