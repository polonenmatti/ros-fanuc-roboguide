In this section we test connections between ROS+RVIZ+MOVIT+Fanuc driver - Fanuc Roboguide.

[Follow this guide](http://wiki.ros.org/fanuc/Tutorials/Running)

Start roboguide, on robot virtual robot run TPE program `rosstate`

Terminal 1: 
`roscore`

Terminal 2:
`roslaunch fanuc_m10ia_support robot_state_visualize_m10ia.launch robot_ip:=localhost use_bswap:=false`

You should see this after:

<img width="2535" height="1373" alt="image" src="https://github.com/user-attachments/assets/a1d2f8a7-ff38-4f31-87ca-094a9bb9b95a" />

And when you move robot from Roboguide teach pendant, robot should move in Rviz too.

Kill processes in terminals ctrl+c.

In roboguide abort running program from robot. FCNT from TP -> Shift + Abort all

Run TP program `ros`

<img width="666" height="195" alt="image" src="https://github.com/user-attachments/assets/1d34f3f4-990c-4b78-840a-5949fd440933" />


Terminal 1: 
`roscore`

Terminal 2:
`roslaunch fanuc_m10ia_moveit_config moveit_planning_execution.launch sim:=false robot_ip:=localhost use_bswap:=false`


