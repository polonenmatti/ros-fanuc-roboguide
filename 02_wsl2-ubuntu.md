This explains the installation of WSL2 and Ubuntu 20.04.

Follow [Install Ubuntu on WSL2](https://documentation.ubuntu.com/wsl/stable/howto/install-ubuntu-wsl2/)

Start powershell terminal.

First do:

`wsl --list --online`

It will install windows subsystem for linux if it's not installed before.

# RESTART YOUR COMPUTER and let windows do updates.

Start powershell terminal again.

`wsl --list --online`

We will install Ubuntu 20.04 with command:

`wsl --install -d Ubuntu-20.04`

It will ask you you make Unix account and choose password.

You should get Welcome to Windows Subsystem for Linux pop-up window. If not, find WSL settings in windows search.

<img width="1093" height="706" alt="image" src="https://github.com/user-attachments/assets/ef645e88-4b5e-417e-bdb5-5fc78456c994" />

Go to Settings -> Networking
Networking mode: Mirrored

This allows to connect localhost rather than some random ip.

Go to Optional Features
Check that Enable GUI applications is ON.


[Continue to ROS-Noetic Install](https://github.com/polonenmatti/ros-fanuc-roboguide/blob/main/03_ros-noetic.md)



