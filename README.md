# ESP32-UR5e Teleoperation and Playback System

## Project Overview
This project implements a teleoperation and playback system for a Universal Robots UR5e robotic arm using an ESP32-S3 microcontroller. The ESP32 acts as a wireless controller, allowing users to record, playback, and visualize robot joint movements and gripper states via a custom hardware interface and a TTGO display. The system is designed for educational, research, and prototyping applications in robotics, automation, and human-robot interaction.

## Features
- **Wireless Teleoperation:** ESP32 connects to a WiFi network and communicates with the UR5e robot and its gripper.
- **Real-Time Control:** Users can control the UR5e's six joints and gripper in real time using potentiometers and buttons.
- **Recording & Playback:** Joint angles and gripper states are sampled and stored for playback, enabling repeatable motion sequences.
- **TTGO Display Visualization:** Real-time feedback of joint angles and Cartesian positions, with multiple visualization modes.
- **Robust Communication:** Handles connection management and error states for both the robot and gripper.

## Hardware Requirements
- **ESP32-S3 Development Board** (with TTGO display)
- **Universal Robots UR5e** (with network access)
- **UR5e-compatible Gripper**
- **Potentiometers** (6x, for joint input)
- **Pushbuttons** (2x, for mode switching and gripper control)
- **Wiring, breadboard, and power supply**

## Software Requirements
- **Arduino IDE** (with ESP32 board support)
- **Libraries:**
  - `TFT_eSPI`
  - `WiFi`
  - `math.h`

## File Structure
- `ProjectGroup7.ino` – Main control logic and state management
- `UR5Control.ino` – Communication and control functions for UR5e and gripper
- `Kinematics.ino` – Joint angle mapping and forward kinematics
- `Graphics.ino` – TTGO display visualization functions
- `ProjectGroup7.h` – Global variables, pin assignments, and function declarations
- `Test.ino` – Experimental and test routines

## Setup & Usage
1. **Hardware Assembly:**
   - Connect potentiometers and pushbuttons to the ESP32-S3 as per pin assignments in `ProjectGroup7.h`.
   - Ensure the TTGO display is properly connected.
2. **Software Installation:**
   - Install the required libraries in the Arduino IDE.
   - Configure WiFi credentials and UR5e IP/port in the code if needed.
   - Upload the code to the ESP32-S3.
3. **Operation:**
   - On boot, the ESP32 connects to WiFi and initializes the display.
   - Use the left button to connect/disconnect to the UR5e and enter control/recording mode.
   - Use the right button to toggle the gripper or enter playback mode.
   - Visual feedback is provided on the TTGO display.

## Contribution Guidelines
- Fork the repository and create feature branches for new contributions.
- Submit pull requests with clear descriptions and testing evidence.
- Report issues or suggest enhancements via GitHub Issues.

## License
This project is released under the MIT License.

## Acknowledgements
- Universal Robots for UR5e documentation
- Espressif for ESP32 platform
- Open-source contributors for Arduino libraries 