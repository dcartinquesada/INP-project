# INP-project
Common errors found during the phase of the installation:

1. ROS1 is not compatible with Ubuntu 22.4: 
  In this case, it was necessary to delete the Ubuntu 22.4 once it was configured in order to switch to Ubuntu 20.4. Due to the fact that ROS1 is an old system, it is better to check its compatibility.
  
2. Memtest86+ stuck at 62%: 
  It appeared a "BSOD"-like warning once I executed "sudo reboot" in order to reboot the computer after all the settings were set up.
  
3. Hardware issue to ThinkPadX220: 
  According to the documentation found in Internet, probably the RAM is failing, so could be important to check the hardware status of the computer before start any installation, as well as trying to improve the components in order to have a better performance. 

Notes about ROS Noetic installation in Ubuntu 20.04:
Specific packages can be found like: 
  sudo at install ros-noetic-PACKAGENAME

AUTOMATIC OPENING:
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc source ~/.bashrc

PREBUILT INSTALLING:
sudo apt-get install ros-noetic-catkin

Then ROS WORKSPACE:
CREATE:
  mkdir -p ~/catkin_ws/src
CHANGE:
  cd ~/catkin_ws/
BUILD:  
  catkin_make
  
ROS PACKAGE:
CHANGE: cd ~/catkin_ws/src

USE THIS IN CASE OF "NO SUCH PACKAGE OR STACK 'BEGINNER_TUTORIALS'"
catkin_create_pkg ultimaker std_msgs rospy roscpp
cd ~/catkin_ws
catkin_make
. ~/catkin_ws/devel/setup.bash
http://wiki.ros.org/ROS/Tutorials/CreatingPackage

Download the talker.py  
wget https://raw.github.com/ros/ros_tutorials/kinetic-devel/rospy_tutorials/001_talker_listener/talker.py

To view and edit the file with  $ rosed beginner_tutorials talker.py 
 

HOW TO SUSCRIBE?
publisher = talker
suscriber = listener
Create a workspace as well as a package (catkin Build System)


Command to see ROS Computation Graph: 
rosrun rqt_graph rqt_graph

Make the catkin package:
  .txt
  .xlm

Make the folder to save the Python/ROS:



HOW TO CREATE A NODE IN ROS:
Node: can communicate with other nodes through services and topics.

HOW TO CREATE A SERVICE IN ROS:
Service:

HOW TO CREATE A TOPIC IN ROS:
Topic:

HOW TO SUSCRIBE TO A TOPIC IN ROS:
In Python each subscriber is running in a different thread and therefore there the only thing that rospy.spin() does is block the main thread from returning and thus keep the subscriber threads alive. 

To close the session, use:
  rosout

FIRST STEPS:
rosrun (ROS command to run a node) turtlesim (ROS package where the ROS node is located) turtlesim_node (ROS node to execute)

In order to understand a topic or a node, use the command: rostopic info ********** 
To see the content of the message when it is published:
  rostopic echo ****
  
To see the message:
rosmsg show geometry_msgs/Twist (topic name)

rostopic echo /turtle1/pose

. ~/catkin_ws/devel/setup.bash


RELATED TO THE HARDWARE:
Once the Ultimaker was connected, it displayed a message related to a port connection: TEMP PORT ERROR: BED.
It was solved simulating a "temperature sensor" with a resistance of 100 Ohm.

Once the electronic part is fixed, there's a new error message related to the software. ERROR MESSAGES:
-E: Unable to locate packages
Once the terminal is open:
bash: /opt/ros/kinetic/setup.bash: No such file or directory
bash: /opt/ros/kinetic/setup.bash: No such file or directory

danniela@danniela-ThinkPad-X220:/etc/ros/rosdep/sources.list.d$ sudo rosdep init
[sudo] password for danniela: 
ERROR: default sources list file already exists:
	/etc/ros/rosdep/sources.list.d/20-default.list
Please delete if you wish to re-initialize
danniela@danniela-ThinkPad-X220:/etc/ros/rosdep/sources.list.d$ sudo rm /etc/ros/rosdep/sources.list.d/20-default.list
danniela@danniela-ThinkPad-X220:/etc/ros/rosdep/sources.list.d$

SO the github .zip is downloaded again in order to complete the installation.

In order to add the source command: $ echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
Use this link to clone the repository: https://github.com/ad0409/open-laboratory-environment.git

cd ~/catkin_ws/src
git clone -b noetic-devel https://github.com/ad0409/open-laboratory-environment.git

And to verify ROS version:  echo $ROS_DISTRO
Do not forget to execute: source ~/catkin_ws/devel/setup.bash

Error when executing .py with rosrun:
[rosrun] Couldn't find executable named /opt/ros/noetic/share/rospy//opt/ros/noetic/share/rospy/open-laboratory-environment/ultimaker_talker.py

I tried with "echo" in order to verify it exists; it shows correctly. But once it is trying to find the path with the ROS commands, it doesn't work.
It is necessary to check CMake. 

If the error message received is the following one:
Unable to register with master node [http://localhost:11311/]: master may not be running yet. Will keep trying.
Then try first: "roscore", in order to start any ROS runnning.

