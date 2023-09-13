# sensor_fusion-for-mobile-robots-using-robot_localization-
# Robot Localization with IMU (BNO055) and GPS RTK using ROS

## Introduction

This repository provides guidance on configuring and using ROS packages for sensor fusion using an IMU (BNO055), SparkFun GPS RTK module, and the Robot Localization package. The fusion of data from these sensors enhances the accuracy of robot localization and navigation.

## Prerequisites

- ROS Noetic installed on your system.

## Packages Used

1. **ros_imu_bno055**: A ROS package for interfacing with the BNO055 IMU sensor.

    - GitHub Repository: [ros_imu_bno055](https://github.com/RoboticArts/ros_imu_bno055.git)
    - Installation instructions and usage are available in the package's README.

2. **ublox_utils**: A ROS package for configuring and interfacing with the SparkFun GPS RTK module.

    - GitHub Repository: [ublox_utils](https://github.com/ethz-asl/ublox_utils.git)
    - Installation instructions and usage are available in the package's README.

3. **robot_localization**: A ROS package for sensor fusion and robot state estimation.

    - GitHub Repository: [robot_localization](https://github.com/cra-ros-pkg/robot_localization)
    - Detailed instructions for configuration and usage are provided below.

## Robot Localization Setup

1. Clone the `robot_localization` package into your ROS workspace:

    ```shell
    cd ~/catkin_ws/src
    git clone https://github.com/cra-ros-pkg/robot_localization.git
    ```

2. Build the ROS workspace:

    ```shell
    cd ~/catkin_ws
    catkin_make
    ```

3. Launch the Robot Localization node with your IMU and GPS RTK topics:

    ```shell
    roslaunch robot_localization ekf_template.launch
    ```

4. Configure the EKF parameters in the launch file to use the topics provided by `ros_imu_bno055` and `ublox_utils`.

## Usage

1. Start your robot's ROS nodes to publish IMU and GPS RTK data.

2. Launch the Robot Localization node as mentioned in the previous section.

3. Visualize the robot's estimated pose using visualization tools like RViz.

## Example Applications

- Use this setup for accurate robot localization in outdoor or GPS-denied environments.
- Implement autonomous navigation algorithms with improved localization accuracy.

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgments

- Special thanks to the authors and maintainers of the `ros_imu_bno055`, `ublox_utils`, and `robot_localization` packages for their contributions to the ROS community.
