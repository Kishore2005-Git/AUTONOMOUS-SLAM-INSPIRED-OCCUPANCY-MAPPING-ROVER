Project Overview

The **Autonomous SLAM-Inspired Occupancy Mapping Rover** is an Arduino Uno-based robotic rover prototype designed to explore the fundamental concepts of autonomous navigation, environmental sensing, and future occupancy-grid mapping.
The rover uses an ultrasonic distance sensor mounted on an SG90 servo motor to scan its surroundings across a 180° field of view. Distance measurements are collected at different angular positions and transmitted to the Serial Monitor.
A dual H-bridge L293D motor driver controls two DC geared motors using a differential-drive mechanism, allowing the rover to move forward, backward, and stop.
The project is developed and simulated using **Tinkercad Circuits** to verify component integration, motor control, ultrasonic sensing, and servo-based environmental scanning.

Project Objectives

- Design a two-wheel differential-drive robotic rover.
- Interface an Arduino Uno with an L293D motor driver.
- Implement forward, backward, and stop motor operations.
- Measure surrounding object distances using an ultrasonic sensor.
- Mount the ultrasonic sensor on an SG90 servo motor for directional scanning.
- Scan the environment from 0° to 180° at 30° intervals.
- Display angular positions and corresponding distance measurements through the Serial Monitor.
- Establish a foundation for future autonomous navigation and SLAM implementation.

Software Requirements

- Arduino IDE or Arduino programming environment
- Tinkercad Circuits
- Arduino Servo Library
- Serial Monitor (9600 baud)

**Programming Language:** Embedded C/C++ (Arduino)

### Serial Monitor Output

The program reports:
- Rover circuit initialization message
- Motor movement status
- Scanning angle
- Corresponding distance measurement
- No-echo status when a valid measurement is unavailable

Example output format:

```text
Rover circuit test started

Moving forward
Moving backward

Angle: 0 degrees, Distance: XX.XX cm
Angle: 30 degrees, Distance: XX.XX cm
Angle: 60 degrees, Distance: XX.XX cm
Angle: 90 degrees, Distance: XX.XX cm
Angle: 120 degrees, Distance: XX.XX cm
Angle: 150 degrees, Distance: XX.XX cm
Angle: 180 degrees, Distance: XX.XX cm
```

Future Enhancements

The project can be extended through the following development stages:
### Stage 1 – Autonomous Obstacle Avoidance
Implement a 20 cm obstacle detection threshold. The rover will stop, reverse when necessary, compare left and right clearances, and select a safer direction.

### Stage 2 – Improved Environmental Scanning
Reduce the angular scanning interval from 30° to smaller steps to obtain more detailed environmental measurements.

### Stage 3 – Coordinate Conversion
Convert the measured distance and scanning angle into Cartesian coordinates:

```text
x = d × cos(θ)
y = d × sin(θ)
```

### Stage 4 – Occupancy Grid Mapping
Use the calculated coordinates to generate a two-dimensional grid representing occupied, free, and unknown regions.

### Stage 5 – Robot Localization
Integrate wheel encoders and an Inertial Measurement Unit (IMU) to estimate the rover's position and orientation.

### Stage 6 – SLAM Implementation
Integrate sensor measurements, robot pose estimation, and mapping techniques to develop a complete Simultaneous Localization and Mapping system.

Applications

- Educational autonomous robotics platforms
- Embedded systems and microcontroller learning
- Indoor environmental scanning
- Basic mobile robot navigation research
- Low-cost robotics prototyping
- Foundation for autonomous exploration systems

Current Limitations

- The project has been developed in a simulation environment and has not yet undergone physical hardware testing.
- Distance measurements are collected but are not currently used to control movement automatically.
- The current implementation does not perform complete obstacle avoidance.
- Scanning resolution is limited to 30° intervals.
- Blocking delays reduce the responsiveness of the program.
- Wheel encoders and IMU-based pose estimation are not implemented.
- No occupancy grid or environmental map is generated.
- Complete robot localization and SLAM are not implemented.


