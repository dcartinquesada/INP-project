# INP-project
Common errors found during the first phase of the installation:

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




HOW TO SUSCRIBE?
publisher = talker
suscriber = listener
1. Create a workspace as well as a package (catkin Build System)
2. 


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

