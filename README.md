# ROS2 Mobile Robot (Inspection Robot)

This project is a ROS2-based mobile robot system built around a differential drive setup. It integrates low-level hardware control using Arduino with higher-level functionalities like SLAM and visualization.

The goal of this project was to understand how a complete robotics pipeline works — from sending motor commands to building and visualizing maps in real time.

---

## What’s in this project i.e: important

The workspace contains multiple ROS2 packages that work together:

* `diffdrive_arduino`
  Handles communication between ROS2 and the Arduino. It is responsible for sending velocity commands and receiving encoder data.

* `inspection_robot`
  Main package that includes the robot description (URDF), launch files, and configurations.

* `visualization_tutorials`
  Used for RViz-based visualization and understanding markers and robot states.

* `serial` and `serial_motor_demo`
  Support packages for serial communication and motor interfacing.

---

## What it does

* Controls a differential drive robot using ROS2
* Interfaces with Arduino for motor control
* Publishes and subscribes to velocity and encoder topics
* Builds a map using SLAM
* Visualizes robot state and environment in RViz

---

## How to run

Clone the repository and build the workspace:

```
cd ~/dev_ws
colcon build
source install/setup.bash
```

Launch the robot:

```
ros2 launch inspection_robot <your_launch_file>.launch.py
```

Run SLAM (if using slam_toolbox):

```
ros2 launch slam_toolbox online_async_launch.py
```

---

## Notes

* This project was developed as part of learning ROS2 and mobile robotics concepts.
* The focus is on understanding system integration rather than production-level deployment.
* Some packages are adapted and modified for learning purposes.

---

## Future improvements

* Navigation stack (Nav2 integration)
* Better hardware abstraction
* GPS-free localization using vision (planned)
* Cleaner package separation and documentation

---

## Author

Pratyush Vatsa
