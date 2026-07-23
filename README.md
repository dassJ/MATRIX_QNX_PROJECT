# M.A.T.R.I.X. – Model-in-the-Loop Advanced Teleoperated Robotic Interface with RTOS eXperimentation

## Project Overview

M.A.T.R.I.X. is a Model-in-the-Loop robotic arm simulation platform developed to demonstrate the practical differences between RTOS and NON-RTOS execution. The project integrates QNX Neutrino RTOS, Python, and a browser-based 3D dashboard to simulate a 5-DOF robotic arm with real-time motion control, emergency stop functionality, and sequence recording.

The system enables users to visualize robotic arm movements, compare deterministic RTOS scheduling with sequential NON-RTOS execution, and observe the effect of real-time task prioritization.

## Problem Statement

Understanding Real-Time Operating Systems through theory alone can be difficult. Existing robotic simulations often fail to demonstrate the practical impact of deterministic scheduling, task preemption, and emergency response. A platform is needed to visualize and compare RTOS and NON-RTOS behaviour in an interactive environment.

## Solution

The project provides a complete Model-in-the-Loop simulation that combines a QNX-based real-time controller, a Python communication bridge, and a Three.js web dashboard. Users can manually control the robotic arm, record motion sequences, replay them through QNX, and compare system behaviour in RTOS and NON-RTOS modes.

## Features

- 5-DOF robotic arm simulation
- Manual joint control
- Teach-and-record motion sequences
- RTOS and NON-RTOS execution modes
- Emergency stop functionality
- Real-time telemetry
- Interactive 3D visualization
- Axis calibration for imported STL models
- TCP and WebSocket communication

## Technologies Used

### Programming Languages

- C
- Python
- JavaScript
- HTML
- CSS

### Frameworks & Libraries

- Three.js
- WebSocket
- TCP Sockets

### Software & Tools

- QNX Neutrino RTOS 8.0
- QNX Momentics IDE
- Visual Studio Code
- VMware
- Git & GitHub

## System Architecture

The system consists of three main components:

- **QNX RTOS Controller** – Executes motion and safety tasks using POSIX real-time threads.
- **Python Bridge** – Transfers data between QNX and the browser using TCP and WebSocket communication.
- **Web Dashboard** – Displays the robotic arm, records poses, and provides manual control.

## Working Principle

1. The user controls the robotic arm through the browser dashboard.
2. Motion sequences are recorded and transmitted to the Python bridge.
3. The bridge forwards the sequence to the QNX RTOS controller.
4. QNX executes each pose using real-time scheduling.
5. Joint positions are continuously transmitted back to the dashboard for live visualization.
6. Emergency stop commands immediately interrupt motion in RTOS mode through task preemption.

## Performance Highlights

- End-to-end latency: **15–20 ms**
- Motion update period: **100 ms**
- RTOS emergency response: **~28 ms**
- NON-RTOS emergency response: **220–380 ms**
- Smooth simultaneous joint movement in RTOS mode
- Visible jitter in NON-RTOS mode under system load

## Applications

- RTOS education
- Robotics research
- Embedded systems learning
- Model-in-the-Loop simulation
- Industrial automation training

## Learning Outcomes

- Real-Time Operating Systems
- POSIX Thread Scheduling
- TCP/IP Communication
- WebSocket Communication
- Three.js Visualization
- Multi-threaded Programming
- Robot Motion Control

## Future Improvements

- Physical robotic arm integration
- ROS 2 support
- Inverse kinematics
- Collision detection
- Multi-user remote control
- Cloud-based monitoring

## Project Report

The complete project documentation, implementation details, system design, experimental results, and performance analysis are available below.

📄 [MATRIX Project Report](MATRIX_PROJECT_REPORT.pdf)

## Conclusion

M.A.T.R.I.X. demonstrates the practical advantages of Real-Time Operating Systems by providing an interactive robotic arm simulation platform. The project successfully visualizes deterministic scheduling, task preemption, and emergency handling while highlighting the performance differences between RTOS and NON-RTOS execution in a realistic environment.
