# Project 3: DC Motor Speed Controller

## Day 1 — System Design

### Objective
Control the speed of a DC motor using an Arduino and PWM, starting with open-loop control.

### System Components

- **Potentiometer:** Provides the user's speed request.
- **Arduino Uno:** Reads the potentiometer and generates a PWM signal.
- **NMOS:** Acts as an electronic switch to control motor current.
- **DC motor:** Converts electrical energy into rotation.
- **External power supply:** Provides energy to the motor.
- **Diode:** Provides a path for inductive current when the motor is switched off, when correctly selected and connected.

### System Block Diagram

Potentiometer → Arduino Uno → PWM → NMOS → DC Motor

The external power supply provides energy through the motor's power circuit.

### Control and Power Paths

**Control path:** Potentiometer → Arduino → PWM signal → NMOS gate.

**Power path:** External supply → switching circuit → DC motor.

The Arduino provides the control signal, while the external supply provides the motor's energy.

### Why Start with an NMOS?

A suitable N-channel MOSFET can switch motor current in response to an Arduino PWM signal. A basic single-MOSFET circuit is suitable for learning one-direction speed control.

An H-bridge will be considered later when forward and reverse motor control are introduced.

The NMOS must be suitable for the motor's voltage and current and must turn on properly with the Arduino's control voltage.

### Learning Outcomes

- Distinguished the control path from the power path.
- Explained why a motor should not be powered directly from an Arduino GPIO pin.
- Understood how PWM duty cycle influences motor speed.
- Distinguished a basic MOSFET switching circuit from an H-bridge driver.

### Tinkercad Component Inventory

- Arduino Uno: Available
- DC motor: Available
- Potentiometer: Available
- NMOS: Available
- Diode: Available
- H-bridge motor driver: Available

### Current Status

Day 1, Lesson 1 completed. No circuit wiring or code has been started.

### Next Step

Inspect the NMOS and motor connections, confirm the power requirements and protection arrangement, and then design the circuit before wiring it in Tinkercad.