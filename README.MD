# mec_mobile #

This repository is for creating a Mecanum Mobile Robot with URDF and Visualize it in RViz.

- Platform: ROS2 Jazzy + Gazebo Harmonic

[Here is the step by step tutrorial video on Youtube](https://youtu.be/ABLQZkkTKlI)

Use the main branch as the start package for Gazebo simulation

## Quick Start

* Create a ros workspace
    ```bash   
    mkdir -p ~/ros2_ws/src
    cd ~/ros2_ws/src
    ```
* Download the package
    ```bash    
    git clone -b main https://github.com/roboticslabs/mec_mobile.git
    ```
* Compile the package
    ```bash
    cd ~/ros2_ws
    sudo apt-get install ros-${ROS_DISTRO}-urdf-tutorial
    colcon build
    ```
* Try it
    ```bash
    source ~/ros2_ws/install/setup.bash
    ros2 launch urdf_tutorial display.launch.py model:=/home/robotlabs/ros2_ws/src/mec_mobile/mec_mobile_description/urdf/robots/robot_3d.urdf.xacro
    ```
