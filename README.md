# ROS2 Humble Setup & Turtlesim Demo

## About This Project

In this project, I installed ROS2 Humble on Ubuntu 22.04 using VirtualBox and tested different ROS2 features including nodes, topics, services, and Turtlesim.

This project demonstrates a complete ROS2 setup and basic interaction between nodes.

---

# Step 1: Install VirtualBox

I downloaded VirtualBox from:

https://www.virtualbox.org/wiki/Downloads

Then I installed it on Windows.

---

# Step 2: Install Ubuntu 22.04

I downloaded Ubuntu 22.04:

https://releases.ubuntu.com/jammy/

Then I created a new Virtual Machine with the following configuration:

- Type: Linux  
- Version: Ubuntu (64-bit)  
- RAM: 4GB  
- CPU: 4 cores  
- Disk: 25GB (Dynamically allocated)

After installation, the system was ready for ROS2 setup.

---

# Step 3: Install ROS2 Humble

First, I updated the system:

```bash
sudo apt update && sudo apt upgrade -y
```

```Then I Installed the ROS2 Desktop & ROS-Base &Development tools:
sudo apt install ros-humble-desktop
sudo apt install ros-humble-ros-base
sudo apt install ros-dev-tools
```

```Then I sourced ROS2:
source /opt/ros/humble/setup.bash
echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
```
---

# Step 4: Test ROS2 Communication

I tested ROS2 using demo nodes.

The listener successfully received messages from the talker.

---

# Step 5: Run Turtlesim
```I installed turtlesim:
sudo apt install ros-humble-turtlesim -y
```
```Then I launched it:
ros2 run turtlesim turtlesim_node
```
```To control the turtle:
ros2 run turtlesim turtle_teleop_key
```
I used the arrow keys to move the turtle.

---

# Step 6: Spawn a Second Turtle
I used the /spawn service to create another turtle inside the simulation.

---

# Step 7: Change Turtle Drawing Color
I used the /turtle1/set_pen service to modify the drawing color.

---

# Step 8: Control Turtle 2 Using Remapping
```To control the second turtle, I remapped the velocity topic:
ros2 run turtlesim turtle_teleop_key --ros-args --remap turtle1/cmd_vel:=/turtle2/cmd_vel
```

---
# Tools Used

- VirtualBox
- Ubuntu 22.04
- ROS2 Humble
- Turtlesim
- rqt
