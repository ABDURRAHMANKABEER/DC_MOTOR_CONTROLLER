# Project 3: DC Motor Speed Controller

## 1. Project Overview

This project focuses on designing and simulating a DC motor speed controller using an Arduino. The goal is to understand how embedded software interacts with electronic circuits to control a physical system.

The project will begin with basic motor switching and gradually progress to PWM-based speed control and closed-loop speed regulation using feedback.

The project will be developed step by step in Tinkercad Circuits, with the circuit design, code, tests, observations, and improvements documented using Git and GitHub.

## 2. Project Objectives

By the end of this project, I aim to:

- Understand the basic operation of a DC motor and its electrical requirements.
- Understand why a motor should not be powered directly from an Arduino GPIO pin.
- Learn how to use a MOSFET or an H-bridge motor driver to control a motor.
- Understand PWM (Pulse Width Modulation) and duty cycle.
- Control motor speed using a potentiometer.
- Use serial communication to observe readings and debug the program.
- Understand the difference between open-loop and closed-loop control.
- Learn how to measure motor speed using a suitable speed sensor or encoder, if supported by the simulation.
- Implement a basic feedback controller that adjusts the motor output based on the difference between the target and measured speeds.
- Develop good engineering practices through circuit design, testing, debugging, and technical documentation.

## 3. System Design

### Initial System: Open-Loop Speed Control

The initial system will use a potentiometer to set the requested motor speed.

**System flow:**

Potentiometer → Arduino → PWM signal → Motor driver or switching circuit → DC motor

The potentiometer provides an input to the Arduino. The Arduino processes the reading and generates a PWM signal. The motor driver or switching circuit controls the current supplied to the motor.

In this stage, the actual motor speed will not be measured by the controller.

### Advanced System: Closed-Loop Speed Control

The system will later be extended to use speed feedback.

**System flow:**

Target speed + Measured speed → Controller → Motor driver → DC motor → Speed sensor → Feedback

The controller will compare the requested speed with the measured speed and adjust the motor output accordingly.

This will introduce the concepts of setpoint, feedback, error, and control action.

## 4. Project Tools

- **Tinkercad Circuits:** Circuit construction and simulation.
- **VS Code:** Writing and editing code and project documentation.
- **Arduino Uno:** Main microcontroller for the simulated system.
- **DC motor:** The system's actuator.
- **Potentiometer:** Manual speed input.
- **MOSFET or H-bridge motor driver:** Motor switching and control.
- **Diode:** Motor transient protection where required by the selected circuit.
- **Git and GitHub:** Version control and project history.

The exact driver circuit and component connections will be selected after inspecting the available simulated components and their pinouts.

## 5. Learning Plan

| Stage | Focus |
|---|---|
| Days 1–3 | System design, motor operation, driver selection, and basic motor switching |
| Days 4–5 | PWM, duty cycle, and potentiometer-based speed control |
| Day 6 | Code improvement, serial debugging, and startup behaviour |
| Days 7–8 | Speed measurement, RPM, and control error |
| Day 9 | Basic closed-loop speed regulation |
| Day 10 | Testing, documentation, and final review |

This is an initial plan, not a strict deadline. Additional sessions will be used when necessary to understand a concept or resolve a circuit or software problem.

If the simulator does not support the required speed-feedback component, the limitation will be documented and an appropriate alternative will be considered.

## 6. Engineering Concepts

### Electronics
- DC motor electrical characteristics
- MOSFET switching and H-bridge operation
- Motor power supply and current requirements
- Common ground and control-signal reference
- Flyback and transient protection
- Basic motor electrical noise considerations

### Embedded Systems
- Arduino inputs and outputs
- `analogRead()`
- PWM output and duty cycle
- Mapping input values to control outputs
- Functions and code organisation
- Timing, sampling, and serial debugging

### Control Engineering
- Open-loop and closed-loop systems
- Target speed and measured speed
- Feedback and control error
- Basic error-based control
- The relationship between PWM, motor speed, and load

## 7. Testing and Evaluation

The system will be tested progressively rather than assembled all at once.

Planned tests include:

- Confirming that the motor can be switched on and off.
- Testing the motor at different PWM duty cycles.
- Checking whether the potentiometer changes the motor output as expected.
- Observing startup behaviour and any minimum duty cycle required to start the motor.
- Measuring speed if suitable simulation support is available.
- Testing whether feedback control reduces the difference between target and measured speed.

Observations, unexpected behaviour, errors, and fixes will be documented as part of the engineering process.

## 8. Project Deliverables

- Project overview and system block diagram
- Circuit schematic or clearly documented circuit connections
- Working simulation
- Readable and explained Arduino code
- Testing results and observations
- Daily learning notes
- Git commits showing development progress
- Final project summary describing the design, challenges, and lessons learned

## 9. Development Approach

The project will follow a practical, incremental learning process:

1. Understand the concept before implementing it.
2. Design the circuit before writing the control program.
3. Test individual parts before integrating the complete system.
4. Explain and understand the code rather than copying it blindly.
5. Debug problems systematically and document the solutions.
6. Review each stage before moving to the next.
7. Use Git to maintain a record of changes and improvements.

## 10. Current Status

- **Project stage:** Day 1 — System design and component inspection
- **Development mode:** Simulation only
- **Simulator:** Tinkercad Circuits
- **Microcontroller:** Arduino Uno
- **Components located:** DC motor, potentiometer, Arduino Uno, MOSFET, diode, and H-bridge motor driver
- **Current milestone:** Understand the system and select a suitable motor-control circuit before wiring and programming.

## 11. Expected Outcome

The expected outcome is a simulated DC motor speed controller that demonstrates the relationship between electronic hardware, embedded programming, and control engineering.

The project should provide a foundation for future work involving motor control, robotics, embedded systems, and more advanced feedback-control applications.
