# ros-fanuc-roboguide
Uef summer school industrial robotics and automation project. In this project I tried to get simulated fanuc robot connected with ROS stack.

Setup:
- 1 PC only
- Windows 11 host running Fanuc Roboguide simulating Fanuc M-10iA robot
- WLS2 installtion of Linux Ubuntu 20.04 running ros-noetic (ROS 1)
- ROS industrial community driver for Fanuc
    - TPE & Karel programs are (documented) for fanuc controller v 7.70
 
Prequisites:
- Windows 11 installed with local administor rights
- Download trial of Roboguide from Fanuc (you might have to contact fanuc to be able to download it). Preferably you should have licence.

Install robuguide.
During process when asking process plugins, select at least HandlingPRO.

<img width="501" height="391" alt="Image" src="https://github.com/user-attachments/assets/8a4d8a27-8027-426d-8310-55ea7722009d" />

Select at least FRVRC V7.70 when asked for FANUC Robotics Virtual Robot Selection
