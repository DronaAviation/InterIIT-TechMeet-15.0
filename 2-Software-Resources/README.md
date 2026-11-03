# Software Resources

Use the **Pluto ROS 2 package**, **Magis V2 firmware** and **PlutoControl Python library** as your primary interfaces to the Pluto hardware. If you add other libraries, modules or dependencies, test them against the Pluto hardware and software environment and document them in your submission.

| Resource | Platform |
|---|---|
| [Magis V2 firmware](#magis-v2-firmware) | Pluto flight controller; built and flashed with Pluto IDE |
| [MagisV2 Wiki](#magisv2-wiki-api-reference) | Firmware API reference |
| [Pluto IDE](#pluto-ide) | VS Code extension |
| [Pluto ROS 2 package](#pluto-ros-2-package) | ROS 2 Foxy, Ubuntu 20.04 or later |
| [ROS 2 tutorial](#ros-2-tutorial) | ROS 2 Humble and Gazebo Fortress, Ubuntu 22.04 only |
| [PlutoControl](#plutocontrol) | Python, installed with pip |
| [eyantra_drone](#eyantra_drone) | ROS 1 (catkin) |
| [dagger](#dagger) | Python, installed from source |

---

## Firmware and IDE

### Magis V2 Firmware

**Repository:** https://github.com/DronaAviation/MagisV2

Open-source flight controller firmware for the Pluto drone family. It is a fork of the Baseflight/Cleanflight stack with a user-facing C++ API: you write your own flight behaviour in `PlutoPilot.cpp` (`plutoInit()`, `plutoLoop()` and related callbacks), and the firmware handles stabilisation, sensor fusion, motor control and communication. The default target is `PRIMUS_X2_v1`.

### MagisV2 Wiki (API Reference)

**Wiki:** https://github.com/DronaAviation/MagisV2/wiki

The full reference for the firmware API. These pages are the most relevant to this challenge:

| Page | Covers |
|---|---|
| [Introduction](https://github.com/DronaAviation/MagisV2/wiki/Introduction) | Firmware architecture and features |
| [PlutoPilot](https://github.com/DronaAviation/MagisV2/wiki/PlutoPilot) | Main system interface and loop management |
| [FC-Control](https://github.com/DronaAviation/MagisV2/wiki/FC-Control) | Flight status, modes and commands |
| [FC-Data](https://github.com/DronaAviation/MagisV2/wiki/FC-Data) | Sensor data and state estimation |
| [FC-Config](https://github.com/DronaAviation/MagisV2/wiki/FC-Config) | PID configuration and system settings |
| [Localisation](https://github.com/DronaAviation/MagisV2/wiki/Localisation) | Position input from external systems (UWB, WhyCon, Vicon) |
| [RC-Interface](https://github.com/DronaAviation/MagisV2/wiki/RC-Interface) | Remote control interface |
| [Debugging](https://github.com/DronaAviation/MagisV2/wiki/Debugging) | Debug output |

### Pluto IDE

**VS Code Marketplace:** https://marketplace.visualstudio.com/items?itemName=Drona-Aviation.pluto-ide

The official VS Code extension for building and flashing Magis V2 firmware. It manages the ARM toolchain, IntelliSense and project setup, so you don't need to clone the firmware repository yourself.

To install it, open VS Code, press `Ctrl+Shift+X`, search for **Pluto IDE** and click **Install**. The [Magis V2 README](https://github.com/DronaAviation/MagisV2#setting-up-with-plutoide) walks through creating a project, selecting the target, building and flashing.

---

## ROS 2

### Pluto ROS 2 Package

**Repository:** https://github.com/DronaAviation/pluto_ros2_package

ROS 2 package for communicating with Pluto drones. Its README is written for ROS 2 Foxy on Ubuntu 20.04 or later.

Connect your computer to the Pluto drone's Wi-Fi, then:

```bash
mkdir -p ~/ros2_ws/src && cd ~/ros2_ws/src
git clone https://github.com/DronaAviation/pluto_ros2_package.git
cd ~/ros2_ws && colcon build
source ~/ros2_ws/install/setup.bash
ros2 run plutodrone plutonode    # prints "Pluto Connected" once it reaches the drone
```

The package README covers the remaining nodes and services.

### ROS 2 Tutorial

**Repository:** https://github.com/DronaAviation/ROS2_Tutorial26

Hands-on ROS 2 labs from Drona Aviation. You drive turtlesim, fly a simulated quadcopter in Gazebo, then fly a real Pluto over Wi-Fi, using the same few lines of Python each time. It is a good starting point for your simulation environment.

It supports **Ubuntu 22.04 with ROS 2 Humble only**. The install script sets everything up in 15–40 minutes:

```bash
git clone https://github.com/DronaAviation/ROS2_Tutorial26.git ~/ROS2_Tutorial
bash ~/ROS2_Tutorial/install.sh
```

---

## Python

### PlutoControl

**PyPI:** https://pypi.org/project/plutocontrol/ · **Source:** https://github.com/DronaAviation/plutocontrol

Python library for communicating with and controlling Pluto drones.

```bash
pip install plutocontrol
```

To fly a Pluto with the keyboard using PlutoControl, see [`task1_builtin_wifi_control.py`](../3-Sample-Code/task1_builtin_wifi_control.py) in `3-Sample-Code/`.

---

## External Projects for Reference

External projects you can refer to for position hold and swarming with Pluto drones.

### eyantra_drone

**Repository:** https://github.com/simmubhangu/eyantra_drone

ROS 1 (catkin) metapackage that controls the drone through ROS topics and services. Its README includes a *Multiple Drones* section on flying several drones on one Wi-Fi network. BSD 2-Clause license.

### dagger

**Repository:** https://github.com/blackbird7112/dagger

Python library for controlling the Pluto drone: connecting, arming and sending RC commands. MIT license.

For position hold, also see the [Localisation](https://github.com/DronaAviation/MagisV2/wiki/Localisation) page of the MagisV2 Wiki, which covers how the firmware accepts position data from an external system.
