# Preparing roboguide 

## Install roboguide.

During process when asking process plugins, select at least HandlingPRO.

<img width="501" height="391" alt="Image" src="https://github.com/user-attachments/assets/8a4d8a27-8027-426d-8310-55ea7722009d" />

Select at least FRVRC V7.70 when asked for FANUC Robotics Virtual Robot Selection and finnish installation process.

## Clone fanuc industrial repo to windows host

Go to `c:\users\%username%\documents\`

Open up GIT Bash

`git clone https://github.com/ros-industrial/fanuc`

## Create roboguide workcell

Start up ROBOGUIDE and start creating new workcell with Workcell Creation Wizard.

Step 1: Give name.

Step 2: Select a new robot with the default HandlingPRO config

Step 3: Robot Software Version V7.70

Step 4: Handlingtool & Set Eoat later.

Step 5: Robot - H863 - M-10iA

Step 6: Next

Step 7: Select Karel (R632) & User Socket Msg (R648)

Step 8: Finish


<img width="760" height="765" alt="image" src="https://github.com/user-attachments/assets/63aa04ba-1e53-4eaa-ad60-cd0e98ac6e9d" />

## Initialize robot

On robot controller initialization:

Robot type: 2. M-10iA

Cable dress-out type: 1

J1 Motion range setting: 1

## Test

From Robot menu -> Interner Explorer check that robot homepage opens in 127.0.0.1

<img width="1238" height="179" alt="image" src="https://github.com/user-attachments/assets/533ee5e1-12ed-46f8-9f41-77150f6fd393" />


Press WIN+R to run `CMD`

`ftp localhost`

press enter (username is not set)

press enter (password is not set)

If all good, you should see:

<img width="493" height="144" alt="image" src="https://github.com/user-attachments/assets/d95b1105-5115-48ed-9fa8-3633c3a3c44d" />

You can exit command line.

## Follow Fanuc industrial driver installation guide step 1

[ROS Wiki Fanuc Tutorials Step 1](https://wiki.ros.org/fanuc/Tutorials)

## Install from source

Add following files to your robot from `c:\users\%username%\documents\fanuc\fanuc_driver\karel\`

<img width="116" height="233" alt="image" src="https://github.com/user-attachments/assets/24bb4e5b-4e18-4459-99bc-7af8bcfdcf37" />

And these too from `c:\users\%username%\documents\fanuc\fanuc_driver\tpe`

<img width="641" height="107" alt="image" src="https://github.com/user-attachments/assets/e5865bbf-6fe3-4afc-b9d4-9c17280a4f2c" />

## Build from source

Build all files:

<img width="510" height="328" alt="image" src="https://github.com/user-attachments/assets/e89938f6-8c1d-4d7c-bb87-6f6125f9cbce" />

Edit List under Export Files:

<img width="514" height="342" alt="image" src="https://github.com/user-attachments/assets/d41fed0a-6443-4977-9d7f-2d26820d1266" />

Select All -> Apply -> Ok

<img width="340" height="455" alt="image" src="https://github.com/user-attachments/assets/29dd2a9a-0d24-449a-ba8b-63e749f65e41" />


Export all to robot:

<img width="549" height="356" alt="image" src="https://github.com/user-attachments/assets/47a8f16c-bbca-45c7-8fad-0d93f3e1d614" />

Under programs you should have (right click programs -> view all):

<img width="165" height="478" alt="image" src="https://github.com/user-attachments/assets/84115735-360a-4c68-a5df-1c95372d1aed" />

## Follow Configuration of the ROS-Industrial driver on Fanuc controllers

[ROS Wiki Fanuc Tutorials Step 2](https://wiki.ros.org/fanuc/Tutorials)

Edit flags:

(Menu→SETUP→Host Comm)
SETUP Servers listing using [SHOW]→Servers

<img width="642" height="440" alt="image" src="https://github.com/user-attachments/assets/a58e37d5-45ed-45f0-883e-f6686c9b9fdc" />

<img width="645" height="443" alt="image" src="https://github.com/user-attachments/assets/9f3f7862-a403-4715-b2b1-7436f41e90e8" />

<img width="633" height="444" alt="image" src="https://github.com/user-attachments/assets/224bb49b-8d53-4998-86c0-7f24998aa573" />

Edit Karel program ros_relay
Select -> Type Karel
and then select ros_relay -> press data -> type KAREL Vars
Select 1 CFG_   RRELAY_CFG_T and press enter

Edit following:
<img width="346" height="319" alt="image" src="https://github.com/user-attachments/assets/031b236a-99bd-449e-9766-081fdc84c9a1" />

Edit Karel program ros_state
Select -> Type Karel
and then select ros_state -> press data -> type KAREL Vars
Select 1 CFG_   RSTATE_CFG_T and press enter

Edit following:
<img width="317" height="240" alt="image" src="https://github.com/user-attachments/assets/8643cc38-6795-4078-a98f-be39d8acafe8" />

If using default PR, R, F no further editing needed.

Next step would be to run programs, but we need to prepape our Linux and ROS-noetic stack.


## Common issues:

<img width="397" height="183" alt="image" src="https://github.com/user-attachments/assets/1e421e17-c9f0-45d4-835e-4740d2a2e996" />

Install .Net Framework 2.0 https://www.microsoft.com/en-us/download/details.aspx?id=6041


Anti-virus & Firewall issues:

<img width="471" height="513" alt="image" src="https://github.com/user-attachments/assets/e42384fb-2e0b-4438-81d7-9cc13155e5d5" />

<img width="897" height="481" alt="image" src="https://github.com/user-attachments/assets/fcdd8e00-c0bd-4703-91f0-e66f8acc262d" />


[Continue to Install WSL2 Linux](https://github.com/polonenmatti/ros-fanuc-roboguide/blob/main/02_wsl2-ubuntu.md)




