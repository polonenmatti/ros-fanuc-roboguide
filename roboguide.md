
Install roboguide.
During process when asking process plugins, select at least HandlingPRO.

<img width="501" height="391" alt="Image" src="https://github.com/user-attachments/assets/8a4d8a27-8027-426d-8310-55ea7722009d" />

Select at least FRVRC V7.70 when asked for FANUC Robotics Virtual Robot Selection and finnish installation process.

Go to `c:\users\%username%\documents\`

Open up GIT Bash

`git clone https://github.com/ros-industrial/fanuc`

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

On robot controller initialization:

Robot type: 2. M-10iA

Cable dress-out type: 1

J1 Motion range setting: 1



From Robot menu -> Interner Explorer check that robot homepage opens in 127.0.0.1

<img width="1238" height="179" alt="image" src="https://github.com/user-attachments/assets/533ee5e1-12ed-46f8-9f41-77150f6fd393" />


Press WIN+R to run `CMD`

`ftp localhost`

press enter (username is not set)

press enter (password is not set)

If all good, you should see:

<img width="493" height="144" alt="image" src="https://github.com/user-attachments/assets/d95b1105-5115-48ed-9fa8-3633c3a3c44d" />

You can exit command line.














Common issues:

<img width="397" height="183" alt="image" src="https://github.com/user-attachments/assets/1e421e17-c9f0-45d4-835e-4740d2a2e996" />

Install .Net Framework 2.0 https://www.microsoft.com/en-us/download/details.aspx?id=6041


Anti-virus & Firewall issues:

<img width="471" height="513" alt="image" src="https://github.com/user-attachments/assets/e42384fb-2e0b-4438-81d7-9cc13155e5d5" />

<img width="897" height="481" alt="image" src="https://github.com/user-attachments/assets/fcdd8e00-c0bd-4703-91f0-e66f8acc262d" />




