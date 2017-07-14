# installROSPX2
Install Robot Operating System (ROS) on NVIDIA DRIVE PX2 (AutoChauffeur)

These scripts will install Robot Operating System (ROS) on the NVIDIA DRIVE PX2.

Tested on Driveinstall V4.1L

The script is based on the Ubuntu ARM install of ROS Kinetic: http://wiki.ros.org/kinetic/Installation/UbuntuARM and Nvidia forum disucssion: https://devtalk.nvidia.com/default/topic/1011002/general/cross-compiling-driveworks-on-the-px2-with-ros/

This script is modified form the https://github.com/JetsonHacks/installROSTX2

Maintainer of ARM builds for ROS is http://answers.ros.org/users/1034/ahendrix/

<strong>updateRepositories.sh</strong>
This is an optional step. Adds the repositories universe, multiverse, and restricted but without perform apt-get update. These repositories are in the standard 27.1 install, so probably not needed.

<strong>installROS.sh</strong>
Adds the ROS sources list, sets the keys and then loads ros-kinetic-desktop. Edit this file to add other ROS packages for your installation. After loading, rosdep is initialized.

<strong>setupCatkinWorkspace.sh</strong>
Usage:

$ ./setupCatkinWorkspace.sh [optionalWorkspaceName]

where optionalWorkspaceName is the name of the workspace to be used. The default workspace name is catkin_ws. This script also sets up some ROS environment variables. Refer to the script for details.

