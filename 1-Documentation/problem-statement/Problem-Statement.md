# Swarm Show Execution Using Pluto Drones

## About Us

Drona Aviation Pvt. Ltd., led by IIT Bombay alumnus Mr. Dinesh Sain, is a leading force in bringing drone technology into India's education landscape. We bring cutting-edge aerial robotics into classrooms through programmable drones, modular learning kits, and hands-on technical workshops designed for practical, experiential STEM learning. As India's leading programmable drone platform with 50,000+ drones deployed globally, our Made-in-India Pluto 1.2 and Pluto X have become trusted tools for learning drone flying, coding, tinkering, prototyping, and real-world innovation. These classroom-safe, curriculum-ready platforms are designed to build future-ready technical skills. Our nationwide impact includes the Atal Drone Module officially adopted by 8,000+ Atal Tinkering Labs under NITI Aayog, bridging academic learning with real drone applications and empowering the young generation of innovators across India.

---

## 1. Problem Statement

Develop a multi-drone swarm platform using Pluto drones that enables coordinated execution of predefined drone formations and synchronized movements.

The solution should integrate swarm coordination, trajectory generation, external vision-based positioning, real-time monitoring, and positional drift correction.

Teams are expected to develop and validate their swarm algorithms in a simulation environment and subsequently demonstrate the same functionality using physical Pluto drones.

The objective is to achieve accurate, synchronized swarm movements while maintaining formation geometry, safe separation, and reliable execution.

## 2. Objectives

- Develop swarm coordination algorithms for multiple Pluto drones.
- Implement synchronized movements and formation control.
- Generate and validate drone trajectories.
- Integrate external vision-based positioning for real-time localization.
- Implement closed-loop position correction to compensate for positional drift.
- Monitor drone positions, trajectories, and system status.
- Validate the developed solution through simulation and physical drone testing.
- Demonstrate a scalable software architecture that can support expansion from four drones towards ten drones.

## 3. Required Swarm Tasks

Teams must implement the following two tasks in both simulation and physical hardware environments.

### Task 1: Line Formation with Wave Effect

- Arrange four drones in a straight-line formation.
- Implement a sequential wave-like movement across the line.
- Ensure coordinated movement and synchronization between all participating drones.
- Maintain the line formation throughout the wave movement.

### Task 2: Circular Formation with Wave Effect

- Arrange four drones in a circular formation.
- Implement a coordinated wave-like movement while maintaining the circular formation.
- Ensure synchronized movement between drones.
- Maintain formation geometry and safe separation throughout the execution.

## 4. Software Development

Teams must develop and validate their swarm coordination solution.

The implementation should include:

- Drone identification and swarm configuration.
- Formation generation and movement logic.
- Synchronized trajectory planning.
- Position and altitude control, subject to hardware capabilities.
- Collision detection and inter-drone separation checks.
- Pre-flight validation of planned movements.
- Simulation-based testing of both required swarm tasks.
- Monitoring of drone positions, trajectories, and formation status.

Teams may use suitable simulation tools and software frameworks. The developed solution should be compatible with the physical Pluto drone platform.

## 5. Physical Drone Testing and Execution

Teams will have the opportunity to test their developed programs on actual Pluto drones through the Airlink platform.

- Students may book testing sessions through the provided Airlink website.
- Testing sessions must be booked in advance using the available booking calendar.
- Session availability will depend on the dates and time slots provided by the organizers.
- Testing will be permitted only during designated working hours.
- Teams must use their booked session time to test, debug, and validate their programs on the physical drones.
- Physical drone access will be subject to availability and the booking schedule.

The final demonstration must be performed using actual Pluto drones provided by Drona Aviation. Both required swarm tasks must be demonstrated on physical hardware.

## 6. External Vision-Based Localization

Teams must integrate the provided external vision-based positioning resources to obtain real-time drone position feedback.

The solution should:

- Identify and track individual drones.
- Estimate drone positions in a common coordinate frame.
- Map camera coordinates to the swarm operating area.
- Associate measured positions with the correct drone identifiers.
- Detect missing, invalid, or outdated position measurements.
- Provide position feedback to the swarm controller.

Teams are responsible for configuring and integrating the positioning system into their solution using the resources and references provided by Drona Aviation.

## 7. Real-Time Monitoring and Drift Correction

During execution, the platform should continuously compare actual drone positions with their target positions and planned trajectories.

Required capabilities include:

- Live visualization of drone positions and trajectories.
- Display of target positions and actual position errors.
- Monitoring of formation accuracy and movement progress.
- Automatic positional drift correction using closed-loop feedback.
- Detection of deviations from planned trajectories.
- Monitoring of inter-drone separation and operating boundaries.
- Logging of flight data and system events.
- Safe handling of localization loss and communication failures.

## 8. Software and Hardware Resources

Drona Aviation will provide the necessary software resources, technical documentation, and hardware-related references to support the development and implementation. These resources will be shared with the participating teams the same day the problem statement is released.

### 8.1 Resources Provided

The available resources will include:

- **Pluto ROS 2 Package:** ROS 2 package and related integration resources for communicating with Pluto drones.
- **Magis V2 Firmware:** Firmware resources required for working with the Pluto platform.
- **Magis V2 Wiki:** API reference for the Magis V2 firmware.
- **Pluto IDE:** VS Code extension for building and flashing Magis V2 firmware.
- **Python Library:** PlutoControl library for drone communication and control.
- **External Positioning System:** Reference implementation, documentation, and relevant resources through a GitHub repository.
- **Airlink Platform:** Access to the Airlink website for booking physical drone testing sessions.

### 8.2 Documentation and Compatibility

The documentation will provide the relevant setup and integration guidance for the supported Pluto software interfaces.

Teams are expected to use the provided Pluto ROS 2 package, Magis V2 firmware, and PlutoControl Python library as the primary software interfaces for hardware integration.

Any additional libraries, modules, or dependencies introduced by the teams must be evaluated and tested for compatibility with the provided Pluto hardware and software environment. Teams are responsible for validating their integrations and documenting any modifications or additional dependencies.

### 8.3 Software Development and Hardware Access

Teams are responsible for developing the swarm algorithms, simulation environment, software integration, and overall implementation.

Physical Pluto drones required for final testing and the final demonstration will be provided by Drona Aviation.

### 8.4 Remote Hardware Testing through Airlink

- Teams must provide a Docker image containing their complete application, dependencies, and configuration files.
- Drona Aviation will prepare the Docker environment and required hardware interfaces on its testing system.
- Teams will receive remote access to their designated environment to deploy, execute, debug, and test their code on actual Pluto drones.
- Drona Aviation will provide the necessary drone IP addresses and communication details.
- Teams must book testing sessions in advance through the Airlink website.
- All specific requirements, including camera calibration, positioning setup, additional dependencies, and configurations, must be communicated at least one working day before the booked session.
- Testing is subject to slot availability and designated working hours.

The airlink sandbox sessions from 16th November onwards, with two slots scheduled per day, each lasting 30 minutes:

- **Slot 1:** 11:00 AM – 12:00 PM
- **Slot 2:** 3:00 PM – 4:00 PM

Sessions will not be conducted on Sundays or 21st November (3rd Saturday), as it is our weekly off.

## 9. Deliverables and Submission Requirements

Teams must submit all deliverables by **5 December 2026**.

### 9.1 Source Code Repository (Mandatory)

Submit a GitHub repository containing:

- Swarm coordination and formation-control algorithms.
- Collision detection and pre-flight validation.
- External positioning and drift correction modules.
- Dockerfile, dependencies, and configuration files.
- README with setup instructions and execution commands.

**Format:** GitHub repository link (public or accessible to organizers).

### 9.2 Physical Demonstration (Mandatory)

Demonstrate both required tasks:

- Line formation with wave effect.
- Circular formation with wave effect.

The team must demonstrate the swarm logic and movement planning. Physical demonstration must validate both tasks using four Pluto drones provided by Drona Aviation.

### 9.3 Technical Documentation (Mandatory)

Submit a report covering:

- System architecture and software design.
- Swarm algorithms and trajectory planning.
- Simulation and hardware integration.
- External positioning and drift correction.
- Safety mechanisms and testing methodology.

**Format:** PDF, maximum 25 pages (excluding cover page and references).

### 9.4 Performance and Testing Report (Mandatory)

Include:

- Simulation and physical testing results.
- Formation accuracy and positional error.
- Synchronization and trajectory performance.
- Inter-drone separation.
- Localization and drift correction performance.
- Limitations and challenges encountered.

**Format:** PDF, maximum 10 pages. Include relevant graphs, tables, and test observations.

### Submission Guidelines

- Clearly distinguish simulation results from physical hardware results.
- Provide complete setup and deployment instructions.
- Submit the Docker image and required configuration details for hardware evaluation.
- Physical execution carries the highest evaluation weight. Simulation-only submissions are eligible for partial marks but do not qualify for full hardware-execution marks.

**Final Submission Deadline: 5 December 2026**

## 10. Evaluation Criteria

The evaluation will give higher weightage to successful execution on physical Pluto drones.

| Evaluation Area | Weight |
|---|---|
| Physical swarm execution and formation accuracy | 40% |
| Localization accuracy and positional drift correction | 20% |
| Synchronization and trajectory execution | 15% |
| Safety mechanisms and fault handling | 10% |
| Simulation, algorithm development, and validation | 10% |
| Software architecture and documentation | 5% |
| **Total** | **100%** |

**Important Evaluation Guidelines:**

- Both required tasks must be demonstrated on physical Pluto drones (which Drona Aviation will bring to the final demonstration) for hardware-execution marks.
- Teams that complete the simulation implementation but are unable to demonstrate the tasks on physical hardware may receive partial marks based on their completed work.

## 11. Expected Outcome

A functional multi-drone swarm platform capable of executing coordinated line and circular formations with wave effects using Pluto drones.

The final solution should demonstrate accurate formation control, synchronized movements, external vision-based localization, real-time monitoring, and automatic positional drift correction on physical hardware.

---

## Resource Links

1. **Magis V2 firmware:** https://github.com/DronaAviation/MagisV2.git
2. **Magis V2 Wiki (API reference):** https://github.com/DronaAviation/MagisV2/wiki
3. **Pluto IDE (VS Code extension):** https://marketplace.visualstudio.com/items?itemName=Drona-Aviation.pluto-ide
4. **ROS 2 Package:** https://github.com/DronaAviation/pluto_ros2_package.git
5. **ROS 2 Tutorial:** https://github.com/DronaAviation/ROS2_Tutorial26.git
6. **PlutoControl:** https://pypi.org/project/plutocontrol/
7. **External projects for reference:**
   - https://github.com/simmubhangu/eyantra_drone.git
   - https://github.com/blackbird7112/dagger.git
8. **Airlink booking:** https://calendar.app.google/5Ao3awEK6FYApRfN6

A guide to each resource, with platform requirements and setup steps, is in [2-Software-Resources](../../2-Software-Resources/README.md).
