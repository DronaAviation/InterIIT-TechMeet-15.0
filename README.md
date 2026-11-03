# InterIIT-TechMeet-15.0
Welcome to the Pluto Drone Swarm Challenge at the Inter IIT Tech Meet 15.0, powered by Drona Aviation. 🚀 This is the official resource hub for the challenge: the problem statement, firmware, software packages, API references and remote-testing details you need to simulate and fly a synchronized swarm of Pluto drones.

---

## The Challenge

Build a multi-drone swarm platform on Pluto drones that flies predefined formations in sync. Your platform tracks each drone with external vision-based positioning and corrects positional drift in closed loop. Develop and validate in simulation first, then demonstrate on four physical Pluto drones.

| Task | Formation | Movement |
|---|---|---|
| **Task 1** | Four drones in a straight line | A sequential wave across the line, keeping the line throughout |
| **Task 2** | Four drones in a circle | A coordinated wave, keeping the circle and safe separation throughout |

Read the full [Problem Statement](1-Documentation/problem-statement/Problem-Statement.md) for the requirements, deliverables and evaluation criteria.

---

## Key Dates

| Date | Event |
|---|---|
| 16 November 2026 | Airlink remote testing sessions begin |
| 5 December 2026 | Final submission deadline |

---

## Quick Links

| Resource | Link |
|---|---|
| Magis V2 firmware | [DronaAviation/MagisV2](https://github.com/DronaAviation/MagisV2) |
| MagisV2 API reference | [MagisV2 Wiki](https://github.com/DronaAviation/MagisV2/wiki) |
| Pluto IDE (VS Code extension) | [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=Drona-Aviation.pluto-ide) |
| Pluto ROS 2 package | [DronaAviation/pluto_ros2_package](https://github.com/DronaAviation/pluto_ros2_package) |
| ROS 2 tutorial | [DronaAviation/ROS2_Tutorial26](https://github.com/DronaAviation/ROS2_Tutorial26) |
| PlutoControl Python library | [PyPI](https://pypi.org/project/plutocontrol/) · [Source](https://github.com/DronaAviation/plutocontrol) |
| External projects for reference | [eyantra_drone](https://github.com/simmubhangu/eyantra_drone) · [dagger](https://github.com/blackbird7112/dagger) |
| Airlink booking | [Booking calendar](https://calendar.app.google/5Ao3awEK6FYApRfN6) |

---

## Repository Structure

### 1. Documentation/
This directory includes all written documents related to the challenge:
- Problem Statement

### 2. Software-Resources/
A guide to each software resource, with platform requirements and setup steps:
- Magis V2 firmware, MagisV2 Wiki and Pluto IDE
- Pluto ROS 2 package and ROS 2 tutorial
- PlutoControl Python library
- External projects for reference

### 3. Sample-Code/
Reference code to get started:
- `task1_builtin_wifi_control.py`: fly the Pluto with the keyboard using the PlutoControl Python library

---

## Remote Hardware Testing (Airlink)

You test your code on real Pluto drones remotely, through the Airlink platform.

1. **Book** a session in advance on the [Airlink booking calendar](https://calendar.app.google/5Ao3awEK6FYApRfN6).
2. **Send your requirements** to Drona Aviation at least one working day before the session: camera calibration, positioning setup, additional dependencies and configuration.
3. **Provide a Docker image** containing your complete application, dependencies and configuration files.
4. **Drona Aviation prepares** the Docker environment and hardware interfaces on its testing system, and shares the drone IP addresses and communication details.
5. **Test in your slot.** You get remote access to deploy, run, debug and test your code on the drones.

Sessions run from 16 November 2026, with two slots a day:

| Slot | Time |
|---|---|
| Slot 1 | 11:00 AM – 12:00 PM |
| Slot 2 | 3:00 PM – 4:00 PM |

There are no sessions on Sundays or on 21 November 2026 (third Saturday, weekly off). Slots are subject to availability.

---

## Submission

Submit everything by **5 December 2026**:

- **Source code repository:** a GitHub link, public or accessible to the organizers, with your swarm, collision-checking, positioning and drift-correction code, plus a Dockerfile, dependencies, configuration files and a README with setup and run commands.
- **Physical demonstration:** both tasks on four Pluto drones provided by Drona Aviation.
- **Technical documentation:** PDF, up to 25 pages excluding the cover page and references.
- **Performance and testing report:** PDF, up to 10 pages, with graphs, tables and test observations.

Physical execution carries the most weight. Simulation-only submissions can earn partial marks, but not the hardware-execution marks. See sections 9 and 10 of the [Problem Statement](1-Documentation/problem-statement/Problem-Statement.md) for details.
