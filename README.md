# Pepper Robot with ROS Indigo

This project involves programming the Pepper robot using ROS Indigo on Ubuntu 14.04 LTS. The code is written in both Python 2.7 and C++ for controlling Pepper's movement, processing sensor data, and implementing robot-human interaction functionalities.

## Table of Contents

- [Overview](#overview)
- [Getting Started](#getting-started)
- [Dependencies](#dependencies)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Overview

This repository contains code to control and interact with the Pepper robot using ROS Indigo. The main objectives of this project are:
- Control Pepper's movements and behaviors.
- Process sensor data (camera, lidar, etc.).
- Develop interaction features using Python 2.7 and C++.

## Getting Started

### Prerequisites

Ensure that you have the following software installed:
- **Ubuntu 14.04 LTS**
- [ROS Indigo](http://wiki.ros.org/indigo)
- Python 2.7
- C++11 or later
- Docker (optional, for containerized development)

### Dependencies

Install the necessary ROS packages:

```bash
sudo apt-get update
sudo apt-get install ros-indigo-desktop-full ros-indigo-moveit ros-indigo-navigation
```

For Python packages:

```bash
pip install -r requirements.txt
```

For C++ dependencies, make sure to install:

- roscpp
- sensor_msgs
- geometry_msgs

## Installation

1) Clone the repository:

```bash
git clone https://github.com/yourusername/pepper-ros-project.git
cd pepper-ros-project
```

2) Initialize your ROS workspace:

```bash
catkin_make
source devel/setup.bash
```

3) Install additional dependencies via rosdep:

```bash
rosdep install --from-paths src --ignore-src -r -y
```

## Usage
### Running the Python Nodes

To run a Python 2.7 node to control Pepper:

```bash
rosrun your_package_name move_pepper.py
```

### Running the C++ Nodes

To compile and run the C++ nodes:

```bash
catkin_make
rosrun your_package_name move_pepper_cpp
```

### Launching with ROS
To launch the entire setup, use the provided launch files:

```bash
roslaunch your_package_name pepper_control.launch
```

## Contributing
Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch (git checkout -b feature-branch).
3. Commit your changes (git commit -am 'Add a new feature').
4. Push to the branch (git push origin feature-branch).
5. Create a new Pull Request.

