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






