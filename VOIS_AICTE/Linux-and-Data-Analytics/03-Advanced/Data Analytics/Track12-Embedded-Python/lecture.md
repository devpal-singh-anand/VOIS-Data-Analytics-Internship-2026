# Getting Started with Embedded Python Programming Using Raspberry Pi Pico

## Learning Objectives

The learning objective is to gain knowledge on:

* understanding the basic details of **Raspberry Pi Pico**.
* understanding different types of sensors.
* understanding the classification of sensors.
* understanding the GPIO pins available on Raspberry Pi Pico.
* programing Raspberry Pi Pico using Python.
* controling input and output devices using GPIO.
* interfacing an LED with Raspberry Pi Pico.
* programing an LED using GPIO.
* understanding ultrasonic/distance sensors.
* interfacing an ultrasonic sensor with Raspberry Pi Pico.
* programing an ultrasonic sensor to detect distance.
* interfacing a switch with Raspberry Pi Pico.
* controling an LED using a switch.
* understanding seven-segment LED displays.
* understanding common-anode and common-cathode seven-segment displays.
* controling individual segments of a seven-segment display.

---

## Prerequisites

Before learning embedded Python programming with Raspberry Pi Pico, you should have:

* Basic knowledge of Python.
* Basic knowledge of Python programming syntax.
* Basic understanding of variables and data types.
* Basic understanding of input and output.
* Basic familiarity with electronic components.
* Basic understanding of electrical circuits is helpful.

---

# About the Course

This course introduces the use of **Python programming for Raspberry Pi Pico** and embedded applications.

The course focuses on programming input and output devices and interfacing sensors with Raspberry Pi Pico.

After completing this course, learners should be able to work with:

* GPIO pins.
* LEDs.
* Switches.
* Ultrasonic/distance sensors.
* Seven-segment displays.
* Other input and output devices.

Python can be used in embedded systems and on small hardware devices where resources are limited.

---

# Embedded Python Programming

Python can be used to program embedded and small hardware devices.

Embedded systems are computing systems designed to perform specific functions.

Depending on the hardware, embedded systems may have limitations such as:

* Limited memory.
* Limited storage.
* Limited processing power.
* Limited power consumption.

Python-based programming environments can simplify the development of applications for compatible embedded hardware.

---

# Types of Sensors

Sensors are devices that detect physical conditions or changes in the environment and convert them into signals that can be processed by a system.

Examples of physical quantities that can be detected include:

* Temperature.
* Distance.
* Light.
* Pressure.
* Motion.
* Sound.
* Humidity.

---

## Classification of Sensors

Sensors can be classified based on the physical quantity they measure and the type of output they produce.

Common examples include:

* Temperature sensors.
* Distance sensors.
* Light sensors.
* Pressure sensors.
* Motion sensors.
* Humidity sensors.
* Proximity sensors.

Sensors allow embedded systems to interact with the physical environment.

---

# Raspberry Pi Pico

**Raspberry Pi Pico** is a development board designed for embedded applications.

It is based on a microcontroller and can be programmed for various input/output applications.

The course focuses on the **Raspberry Pi Pico** and its GPIO capabilities.

---

# Microcontrollers

A **microcontroller** is a small computer integrated into a single chip.

A microcontroller generally contains:

* Processor/core.
* Memory.
* Input/output interfaces.
* Timers.
* Communication peripherals.

Microcontrollers are commonly used in embedded devices.

Examples of embedded applications include:

* Keyboards.
* Sensors.
* Controllers.
* Automation systems.
* Robotics.
* IoT devices.

---

# Raspberry Pi Pico Features

The Raspberry Pi Pico used in the course provides several useful features for embedded programming.

Important features include:

* Dual-core ARM Cortex-M0+ processor.
* Flexible clock running up to approximately **133 MHz**.
* **264 KB SRAM**.
* **2 MB onboard flash memory**.
* USB 1.1 device and host support.
* Low-power sleep and dormant modes.
* Drag-and-drop programming using USB mass storage.
* Multiple multifunction GPIO pins.
* PWM support.
* Accurate clock and timer functionality.
* On-chip temperature sensor.
* Accelerated floating-point libraries.
* Programmable I/O state machines.

These features make Raspberry Pi Pico suitable for embedded programming and hardware interfacing.

---

# Raspberry Pi Pico GPIO

GPIO stands for:

```text
General Purpose Input/Output
```

GPIO pins allow the microcontroller to communicate with external electronic components.

GPIO pins can be configured as:

* Input.
* Output.

Examples of devices that can be connected through GPIO include:

* LEDs.
* Switches.
* Sensors.
* Displays.
* Other electronic components.

---

# Raspberry Pi Pico GPIO Pin Details

The Raspberry Pi Pico board has **40 physical pins**.

GPIO pins are identified using GPIO numbers.

The course refers to GPIO pins for controlling external devices.

An onboard LED is also available on the Raspberry Pi Pico and can be controlled by software.

---

# Setting Up an Online Simulator

The course uses an online simulator for Raspberry Pi Pico programming and circuit demonstrations.

A typical workflow is:

1. Open the online simulator.
2. Select Raspberry Pi Pico.
3. Open the programming/editor area.
4. Enter or copy the Python program.
5. Connect the required electronic components.
6. Run the program.
7. Observe the output.

The simulator allows the circuit and program to be tested without requiring physical hardware.

---

# GPIO Programming with LED

An LED is a common output device used in embedded programming.

LED stands for:

```text
Light Emitting Diode
```

An LED can be turned:

```text
ON
```

or:

```text
OFF
```

using a GPIO output pin.

---

## LED GPIO Programming

The course demonstrates connecting an LED to a GPIO pin and controlling it using Python.

The program generally performs the following operations:

1. Import the required Python packages.
2. Define the GPIO pin connected to the LED.
3. Configure the GPIO pin as an output.
4. Define a delay between ON and OFF states.
5. Set the GPIO value to `1` to turn the LED ON.
6. Set the GPIO value to `0` to turn the LED OFF.
7. Repeat the operation using a loop.

A conceptual example is:

```python
import time
from machine import Pin

led = Pin(28, Pin.OUT)

while True:
    led.value(1)
    time.sleep(1)

    led.value(0)
    time.sleep(1)
```

The exact GPIO number and library syntax depend on the Raspberry Pi Pico programming environment used by the course.

---

## LED GPIO Values

A digital GPIO output generally uses two logical states:

```text
0 → LOW / OFF
1 → HIGH / ON
```

Therefore:

```python
led.value(1)
```

sets the output HIGH, while:

```python
led.value(0)
```

sets the output LOW.

---

## LED Circuit

The LED should be connected to the specified GPIO pin according to the circuit diagram.

The typical circuit includes:

* Raspberry Pi Pico.
* GPIO output pin.
* LED.
* Appropriate resistor.
* Ground connection.

After connecting the circuit:

1. Enter the program.
2. Click the **Run** button.
3. Observe the LED.
4. The LED should turn ON and OFF according to the program.

---

# Ultrasonic Sensor

An **ultrasonic sensor** is an electronic device used to measure the distance of an object.

It works by:

1. Emitting ultrasonic sound waves.
2. Waiting for the waves to reflect from an object.
3. Detecting the reflected signal.
4. Calculating the distance based on the time taken by the signal to return.

Ultrasonic waves travel at a frequency above the range of human hearing.

---

# Working Principle of an Ultrasonic Sensor

The basic process is:

```text
Ultrasonic pulse transmitted
          ↓
Pulse travels toward object
          ↓
Pulse reflects from object
          ↓
Echo received
          ↓
Time is measured
          ↓
Distance is calculated
```

The distance can be calculated using the travel time of the ultrasonic wave.

A commonly used relationship is:

```text
Distance = Speed × Time
```

Because the sound travels to the object and back, the measured time represents a round trip.

Therefore, the distance calculation commonly uses:

```text
Distance = (Speed of Sound × Time) / 2
```

---

# Ultrasonic Sensor Pins

The ultrasonic sensor described in the course has several pins.

Common pins include:

| Pin  | Purpose        |
| ---- | -------------- |
| VCC  | Power          |
| GND  | Ground         |
| TRIG | Trigger signal |
| ECHO | Echo signal    |

The **TRIG** pin is used to initiate the ultrasonic measurement.

The **ECHO** pin provides a signal corresponding to the time taken for the reflected ultrasonic wave to return.

---

# Ultrasonic Sensor Programming

The course demonstrates connecting the ultrasonic sensor to Raspberry Pi Pico.

The circuit uses GPIO pins for:

* Trigger.
* Echo.

The example described in the course uses:

```text
TRIG → GPIO 3
ECHO → GPIO 2
```

The exact wiring should always follow the circuit diagram provided by the course/simulator.

---

## Ultrasonic Sensor Programming Workflow

The general process is:

1. Import the required Python modules.
2. Configure the trigger GPIO as an output.
3. Configure the echo GPIO as an input.
4. Send a trigger pulse.
5. Measure the echo response.
6. Calculate the distance.
7. Display or use the calculated distance.
8. Repeat the measurement if required.

---

# Switch Programming

A switch is an input device.

It can be used to provide a digital signal to Raspberry Pi Pico.

The switch can represent two basic states:

```text
ON / Pressed
OFF / Released
```

The Raspberry Pi Pico reads the switch state through a GPIO input pin.

---

# Switch and LED Practical

The course demonstrates connecting:

* A switch to a GPIO input.
* An LED to a GPIO output.

The example uses:

```text
Switch → GPIO 0
LED    → GPIO 28
```

The program can read the switch and control the LED accordingly.

A conceptual workflow is:

```text
Switch pressed
      ↓
GPIO input detected
      ↓
Program processes input
      ↓
LED GPIO output changes
      ↓
LED turns ON/OFF
```

---

# Seven-Segment Display

A **seven-segment display** is a digital display module used to display numerical information.

It consists of light-emitting diode segments arranged in the shape of a number.

The seven segments are generally identified as:

```text
    a
   ---
f |   | b
   -g-
e |   | c
   ---
    d
```

The individual segments can be switched ON or OFF to create different numbers.

---

# Seven-Segment Display Segments

A seven-segment display contains seven main LED segments:

```text
a
b
c
d
e
f
g
```

By controlling these segments in different combinations, numerical digits can be displayed.

For example, displaying `0` generally requires:

```text
a
b
c
d
e
f
```

while the middle segment:

```text
g
```

remains OFF.

---

# Types of Seven-Segment Displays

There are two common types of seven-segment displays:

1. **Common Anode**
2. **Common Cathode**

---

# Common-Anode Seven-Segment Display

In a common-anode display:

* The anodes of all LED segments are connected to a common terminal.
* The common terminal is connected to the positive supply.
* Individual segments are controlled through their corresponding pins.

The logic required to turn segments ON/OFF depends on the circuit configuration.

---

# Common-Cathode Seven-Segment Display

In a common-cathode display:

* The cathodes of all LED segments are connected to a common terminal.
* The common terminal is connected to ground.
* Individual segments are controlled through their corresponding pins.

Again, the required logic depends on the circuit configuration.

---

# Seven-Segment GPIO Control

The individual segments of a seven-segment display can be connected to GPIO pins.

Through GPIO pins, each segment can be digitally controlled.

Conceptually:

```text
GPIO → Segment a
GPIO → Segment b
GPIO → Segment c
GPIO → Segment d
GPIO → Segment e
GPIO → Segment f
GPIO → Segment g
```

By controlling these pins, different digits can be displayed.

---

# Seven-Segment Display Common Pins

The course explains that the seven-segment display has common terminals.

There are:

```text
2 common pins
```

with one common pin located at the bottom and another at the top of the display package.

The appropriate common terminal must be connected according to the type of display and circuit configuration.

---

# Seven-Segment Display Programming

The seven-segment display can be programmed by configuring its GPIO pins as digital output pins.

The general process is:

1. Import the required Python modules.
2. Define GPIO pins connected to the seven segments.
3. Configure the pins as outputs.
4. Define the required ON/OFF combinations.
5. Set the GPIO values.
6. Display the desired digit.

---

## Example Segment Representation

A conceptual representation can be created using Boolean values:

```text
1 → Segment ON
0 → Segment OFF
```

For example, a digit can be represented by a combination such as:

```text
a b c d e f g
1 1 1 1 1 1 0
```

This corresponds conceptually to displaying:

```text
0
```

The exact logic may be inverted for a common-anode display.

---

# Practical Circuit Workflow

For the practical examples in this course, the general workflow is:

```text
Select Raspberry Pi Pico
        ↓
Open simulator
        ↓
Connect components
        ↓
Configure GPIO pins
        ↓
Write Python program
        ↓
Run program
        ↓
Observe hardware output
```

---

# GPIO Input and Output

GPIO pins can be used for both input and output operations.

## GPIO Output

An output GPIO sends a digital signal to an external device.

Examples:

* LED.
* Display.
* Buzzer.

Conceptually:

```text
Python Program
      ↓
GPIO Output
      ↓
Electronic Device
```

---

## GPIO Input

An input GPIO reads a digital signal from an external device.

Examples:

* Switch.
* Digital sensor.

Conceptually:

```text
Electronic Device
      ↓
GPIO Input
      ↓
Python Program
```

---

# Input and Output Devices

The course demonstrates several input/output devices.

| Device                | Type   | Purpose                        |
| --------------------- | ------ | ------------------------------ |
| LED                   | Output | Displays ON/OFF state          |
| Switch                | Input  | Provides user input            |
| Ultrasonic Sensor     | Input  | Measures distance              |
| Seven-Segment Display | Output | Displays numerical information |

---

# Important Raspberry Pi Pico Concepts

## Raspberry Pi Pico

```text
Microcontroller development board
```

---

## GPIO

```text
General Purpose Input/Output
```

---

## Digital Output

```text
Used to control external devices
```

---

## Digital Input

```text
Used to read external devices
```

---

## LED

```text
Light Emitting Diode
```

---

## Ultrasonic Sensor

```text
Measures distance using ultrasonic sound waves
```

---

## TRIG Pin

```text
Starts an ultrasonic measurement
```

---

## ECHO Pin

```text
Provides the returned ultrasonic signal
```

---

## Seven-Segment Display

```text
Digital display consisting of seven LED segments
```

---

# Common-Anode vs Common-Cathode

| Feature           | Common Anode             | Common Cathode           |
| ----------------- | ------------------------ | ------------------------ |
| Common connection | Anodes                   | Cathodes                 |
| Common terminal   | Positive side            | Ground/negative side     |
| Segment control   | Depends on circuit logic | Depends on circuit logic |
| Main use          | Numerical display        | Numerical display        |

---

# Sensor and Device Examples

The course introduces several examples of hardware interfacing.

```text
Raspberry Pi Pico
       │
       ├── LED
       │
       ├── Switch
       │
       ├── Ultrasonic Sensor
       │
       └── Seven-Segment Display
```

These examples demonstrate how software can interact with physical hardware.

---

# Practical 1 — LED Control

## Objective

Control an LED using a Raspberry Pi Pico GPIO output.

## Components

* Raspberry Pi Pico.
* LED.
* Resistor.
* Jumper wires.
* Ground connection.

## GPIO

The course example uses:

```text
GPIO 28
```

## Process

1. Connect the LED according to the circuit diagram.
2. Configure GPIO 28 as an output.
3. Set the GPIO HIGH.
4. Observe the LED turning ON.
5. Set the GPIO LOW.
6. Observe the LED turning OFF.
7. Repeat using a loop.

---

# Practical 2 — Ultrasonic Distance Sensor

## Objective

Measure the distance of an object using an ultrasonic sensor.

## Components

* Raspberry Pi Pico.
* Ultrasonic sensor.
* Jumper wires.

## GPIO Connections

The course example specifies:

```text
TRIG → GPIO 3
ECHO → GPIO 2
```

## Process

1. Connect power and ground.
2. Connect the trigger pin.
3. Connect the echo pin.
4. Configure trigger as output.
5. Configure echo as input.
6. Send a trigger pulse.
7. Measure the echo time.
8. Calculate the distance.
9. Display/use the result.

---

# Practical 3 — Switch and LED

## Objective

Use a switch as an input to control an LED.

## GPIO Connections

The course example uses:

```text
Switch → GPIO 0
LED    → GPIO 28
```

## Process

```text
Read Switch
     ↓
Check Input
     ↓
Switch Pressed?
   ↙       ↘
 Yes        No
 ↓           ↓
LED ON      LED OFF
```

---

# Practical 4 — Seven-Segment Display

## Objective

Use GPIO pins to control a seven-segment LED display.

## Components

* Raspberry Pi Pico.
* Seven-segment display.
* Appropriate resistors.
* Jumper wires.

## Process

1. Identify the type of seven-segment display.
2. Identify the common terminal.
3. Connect the display segments to GPIO pins.
4. Configure GPIO pins as outputs.
5. Define the required segment combinations.
6. Run the program.
7. Observe the numerical output.

---

# Python Programming Pattern for GPIO

Embedded Python programs commonly follow this structure:

```text
Import modules
      ↓
Configure GPIO
      ↓
Initialize devices
      ↓
Read inputs / generate outputs
      ↓
Process data
      ↓
Repeat if required
```

---

# Example GPIO Program Structure

A basic conceptual program is:

```python
from machine import Pin
import time

device = Pin(28, Pin.OUT)

while True:
    device.value(1)
    time.sleep(1)

    device.value(0)
    time.sleep(1)
```

This structure demonstrates:

* Importing the GPIO library.
* Creating a GPIO object.
* Configuring the pin as output.
* Writing digital values.
* Adding delays.
* Repeating the operation.

---

# Digital GPIO Values

GPIO digital signals commonly use two values:

| Value | State |
| ----- | ----- |
| `0`   | LOW   |
| `1`   | HIGH  |

Depending on the circuit, HIGH or LOW may represent the ON state of a particular component.

Therefore, the circuit configuration must always be considered when interpreting GPIO values.

---

# Embedded System Workflow

A typical embedded application follows:

```text
Physical Environment
        ↓
Sensor / Input Device
        ↓
GPIO Input
        ↓
Raspberry Pi Pico
        ↓
Python Program
        ↓
Processing
        ↓
GPIO Output
        ↓
LED / Display / Actuator
```

---

# Important Terminology

| Term                  | Meaning                                          |
| --------------------- | ------------------------------------------------ |
| Raspberry Pi Pico     | Microcontroller development board                |
| Microcontroller       | Small computer designed for embedded control     |
| GPIO                  | General Purpose Input/Output                     |
| LED                   | Light Emitting Diode                             |
| Sensor                | Device that detects physical conditions          |
| Ultrasonic Sensor     | Sensor used to measure distance                  |
| TRIG                  | Trigger input of ultrasonic sensor               |
| ECHO                  | Echo output of ultrasonic sensor                 |
| Seven-Segment Display | Display made from seven LED segments             |
| Common Anode          | Seven-segment configuration with common anodes   |
| Common Cathode        | Seven-segment configuration with common cathodes |
| Input                 | Signal received by the microcontroller           |
| Output                | Signal generated by the microcontroller          |
| PWM                   | Pulse Width Modulation                           |
| SRAM                  | Static Random Access Memory                      |
| GPIO HIGH             | Digital logic high                               |
| GPIO LOW              | Digital logic low                                |

---

# Quick Reference

| Concept           | Description                                |
| ----------------- | ------------------------------------------ |
| Raspberry Pi Pico | Embedded microcontroller development board |
| GPIO              | General Purpose Input/Output               |
| GPIO Input        | Reads a signal from an external device     |
| GPIO Output       | Controls an external device                |
| LED               | Common output device                       |
| Switch            | Common input device                        |
| Ultrasonic Sensor | Measures distance                          |
| TRIG              | Starts ultrasonic measurement              |
| ECHO              | Returns ultrasonic timing signal           |
| Seven-Segment     | Numerical display                          |
| Common Anode      | Anodes connected to common terminal        |
| Common Cathode    | Cathodes connected to common terminal      |
| Python            | Programming language used in the course    |

---

# Common Knowledge Check Points

Remember:

```text
Microcontroller development board
        ↓
Raspberry Pi Pico

General Purpose Input/Output
        ↓
GPIO

Output device
        ↓
LED

Input device
        ↓
Switch

Distance measurement
        ↓
Ultrasonic Sensor

Ultrasonic measurement start
        ↓
TRIG

Ultrasonic return signal
        ↓
ECHO

Numerical display
        ↓
Seven-Segment Display

Common positive connection
        ↓
Common Anode

Common negative connection
        ↓
Common Cathode

Digital LOW
        ↓
0

Digital HIGH
        ↓
1
```

---

# GPIO Practical Reference

| Practical         | Input  | Output           | Example GPIO               |
| ----------------- | ------ | ---------------- | -------------------------- |
| LED Control       | —      | LED              | GPIO 28                    |
| Ultrasonic Sensor | ECHO   | TRIG             | ECHO GPIO 2, TRIG GPIO 3   |
| Switch + LED      | Switch | LED              | Switch GPIO 0, LED GPIO 28 |
| Seven-Segment     | —      | Display segments | GPIO-controlled segments   |

---

# Practical Workflow

A typical Raspberry Pi Pico project can be summarized as:

```text
Understand the hardware
       ↓
Identify GPIO pins
       ↓
Connect the circuit
       ↓
Import Python modules
       ↓
Configure GPIO
       ↓
Initialize input/output devices
       ↓
Read sensor/input
       ↓
Process the input
       ↓
Generate output
       ↓
Run and test
       ↓
Observe the result
```

---

# Example Complete LED Workflow

## Step 1: Import Required Modules

```python
from machine import Pin
import time
```

---

## Step 2: Configure GPIO

```python
led = Pin(28, Pin.OUT)
```

---

## Step 3: Turn LED ON

```python
led.value(1)
```

---

## Step 4: Wait

```python
time.sleep(1)
```

---

## Step 5: Turn LED OFF

```python
led.value(0)
```

---

## Step 6: Repeat

```python
while True:
    led.value(1)
    time.sleep(1)

    led.value(0)
    time.sleep(1)
```

---

# Example Complete GPIO Concept

```text
Python Program
      ↓
Configure GPIO
      ↓
 ┌─────────────┐
 │ Input GPIO  │
 └──────┬──────┘
        ↓
   Read Device
        ↓
     Process
        ↓
 ┌─────────────┐
 │ Output GPIO │
 └──────┬──────┘
        ↓
   Control Device
```

---

# Course Summary

This course introduced the fundamental concepts of **embedded Python programming using Raspberry Pi Pico**.

The major topics covered were:

* Introduction to embedded Python programming.
* Types and classification of sensors.
* Raspberry Pi Pico.
* Microcontrollers.
* Raspberry Pi Pico features.
* GPIO programming.
* Raspberry Pi Pico GPIO pins.
* Online simulation.
* LED interfacing.
* LED GPIO programming.
* Digital HIGH and LOW states.
* Ultrasonic sensors.
* Distance measurement.
* Ultrasonic sensor pins.
* TRIG and ECHO signals.
* Ultrasonic sensor programming.
* Switch programming.
* Switch and LED interfacing.
* Seven-segment displays.
* Seven-segment LED segments.
* Common-anode displays.
* Common-cathode displays.
* GPIO control of seven-segment displays.
* Practical embedded programming.

The overall concept can be summarized as:

```text
Raspberry Pi Pico
       ↓
GPIO
       ↓
Input / Output Devices
       ↓
Sensors
       ↓
Python Program
       ↓
Processing
       ↓
Output Devices
```

After completing the course, you should be familiar with using Python on Raspberry Pi Pico to interact with GPIO pins, LEDs, switches, ultrasonic distance sensors, and seven-segment displays.

---

# Final Revision

Before attempting the assessment, remember these key facts:

```text
Raspberry Pi Pico
→ Microcontroller development board

GPIO
→ General Purpose Input/Output

GPIO can be configured as
→ Input or Output

LED
→ Light Emitting Diode

LED is generally used as
→ Output device

Switch
→ Input device

Ultrasonic sensor
→ Distance measurement device

TRIG
→ Starts ultrasonic measurement

ECHO
→ Provides returned ultrasonic signal

Seven-segment display
→ Numerical display

Seven-segment types
→ Common Anode and Common Cathode

Common Anode
→ Anodes connected to common terminal

Common Cathode
→ Cathodes connected to common terminal

Digital GPIO states
→ HIGH / LOW
→ 1 / 0
```

---

# Course Completion

Well done! You've completed the course.

You should now be able to:

* Understand the fundamentals of Raspberry Pi Pico.
* Understand microcontrollers and embedded Python programming.
* Identify common types of sensors.
* Understand GPIO pins.
* Program GPIO output devices.
* Interface and control LEDs.
* Interface switches.
* Read digital input.
* Understand ultrasonic distance sensors.
* Work with TRIG and ECHO signals.
* Program distance sensors.
* Understand seven-segment displays.
* Differentiate between common-anode and common-cathode displays.
* Control display segments using GPIO.

Are you ready to check your knowledge?

Click the button below to start the assessment.

You must achieve **80%** to pass the assessment.

If you are not ready for the assessment, review the course material before attempting it.

---

# Course Files

```text
Track12-Embedded-Python-Raspberry-Pi-Pico/
├── lecture.md
├── assessment.md
└── certificate.pdf
```
