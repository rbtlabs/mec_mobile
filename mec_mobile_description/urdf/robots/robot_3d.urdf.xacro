<?xml version="1.0"?>
<robot xmlns:xacro="http://www.ros.org/wiki/xacro" name="robot_3d">

    <xacro:property name="M_PI" value="3.1415926535897931" />

    <xacro:arg name="robot_name" default="robot_3d"/>
    <xacro:arg name="prefix" default=""/>
    <xacro:arg name="use_gazebo" default="false"/>

    <xacro:include filename="$(find mec_mobile_description)/urdf/mech/robot_3d_base.urdf.xacro"/>
    <xacro:include filename="$(find mec_mobile_description)/urdf/mech/mecanum_wheel.urdf.xacro"/>
    <xacro:include filename="$(find mec_mobile_description)/urdf/sensors/rgbd_camera.urdf.xacro"/>
    <xacro:include filename="$(find mec_mobile_description)/urdf/sensors/lidar.urdf.xacro"/>
    <xacro:include filename="$(find mec_mobile_description)/urdf/sensors/imu.urdf.xacro"/>

    <xacro:robot_3d_base prefix="$(arg prefix)"/>

    <xacro:mecanum_wheel
      prefix="$(arg prefix)"
      side="front_left"
      x_reflect="1"
      y_reflect="1"/>

    <xacro:mecanum_wheel
      prefix="$(arg prefix)"
      side="front_right"
      x_reflect="1"
      y_reflect="-1"/>

    <xacro:mecanum_wheel
      prefix="$(arg prefix)"
      side="back_left"
      x_reflect="-1"
      y_reflect="1"/>

    <xacro:mecanum_wheel
      prefix="$(arg prefix)"
      side="back_right"
      x_reflect="-1"
      y_reflect="-1"/>

    <xacro:rgbd_camera
      prefix="$(arg prefix)"
      camera_name="cam_1"
      xyz_offset="0.105 0 0.03"
      rpy_offset="0 0 0"/>

    <xacro:lidar_sensor
      prefix="$(arg prefix)"
      parent="base_link"
      frame_id="laser_frame"
      xyz_offset="0 0 0.0825"
      rpy_offset="0 0 3.14"
      mesh_xyz_offset="0 0 0"
      mesh_rpy_offset="${-M_PI/2} 0 0"
      topic_name="scan"/>

    <xacro:imu_sensor
      prefix="$(arg prefix)"
      parent="base_link"
      frame_id="imu"
      xyz_offset="0 0 0.006"
      rpy_offset="0 0 0"
      update_rate="15.0"
      topic_name="imu/data"/>
    <!--
    <xacro:include filename="$(find mec_mobile_description)/urdf/control/velocity_control_plugin.urdf.xacro" />
    <xacro:load_velocity_control_plugin use_gazebo="$(arg use_gazebo)"/>

    <xacro:include filename="$(find mec_mobile_description)/urdf/control/gazebo_sim_ros2_control.urdf.xacro" />
    <xacro:load_gazebo_sim_ros2_control_plugin
      robot_name="$(arg robot_name)"
      use_gazebo="$(arg use_gazebo)"/>

    <xacro:include filename="$(find mec_mobile_description)/urdf/control/robot_3d_ros2_control.urdf.xacro" />
    <xacro:mec_mobile_ros2_control
      prefix="$(arg prefix)"
      use_gazebo="$(arg use_gazebo)"/>
    -->
    
</robot>