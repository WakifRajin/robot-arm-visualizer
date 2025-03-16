# Robot Arm Visualizer

A ROS2-based GUI application for visualizing and controlling a robotic arm in real time using Tkinter and Matplotlib.

## Features
- **Real-time Joint Angle Visualization**: Updates in response to ROS2 messages.
- **3D Visualization**: Displays the robot arm's movement in 3D using Matplotlib.
- **GUI-based Control**: Adjustable sliders to manually control joint angles.
- **ROS2 Integration**: Subscribes and publishes to the `/joint_angles` topic for synchronization.

## Prerequisites
- ROS2 Humble installed
- Python 3.x
- Required dependencies:
  ```bash
  pip install numpy matplotlib rclpy tkinter
  ```

## Installation & Usage
### Clone the Repository
```bash
git clone https://github.com/WakifRajin/robot-arm-visualizer.git
cd robot-arm-visualizer
```

### Build and Source the ROS2 Workspace
```bash
cd ~/ros2_2025/
colcon build
source install/setup.bash
```

### Run the Visualizer Nodes
#### Start the Joint Angle GUI
```bash
ros2 run arm_visualizer joint_visualizer
```

#### Start the 3D Visualizer
```bash
ros2 run arm_visualizer arm_3d_visualizer
```

## Topics
| Topic Name      | Type                    | Description                              |
|---------------|----------------------|----------------------------------|
| `/joint_angles` | `std_msgs/Float32MultiArray` | Publishes/subscribes joint angles |

## Contributing
Feel free to open issues or submit pull requests to enhance the project.

## License
This project is licensed under the MIT License. See `LICENSE` for details.

## Author
Developed by [Wakif Rajin](https://github.com/WakifRajin).
