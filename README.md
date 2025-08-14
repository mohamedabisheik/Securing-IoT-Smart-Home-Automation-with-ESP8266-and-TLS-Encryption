**Securing IoT Smart Home Automation with ESP8266 and TLS Encryption**
This repository contains the code, schematics, and documentation for an MSc project focused on building a secure IoT smart home automation system using an ESP8266 NodeMCU, a 4-channel relay module, and the Sinric Pro cloud platform with TLS encryption.

**Project Overview**
The system enables remote control of home appliances (e.g., charger, fan, light) via a web dashboard, voice commands, and manual switches, with a manual emergency cutoff for safety. Security is ensured through TLS encryption and API key authentication. The project includes hardware assembly, software configuration, and testing, completed between June and August 2025.

**Features**
Remote Control: Manage devices via the Sinric Pro dashboard.
Voice Control: Integrate with voice assistants through Sinric Pro.
Manual Control: Use physical switches for direct operation.
Security: TLS encryption and API key checking for secure communication.
Safety: Emergency power cutoff switch.
Monitoring: Real-time status updates to the dashboard.

**Repository Contents**
src/: Arduino/C++ code for the ESP8266 NodeMCU (e.g., main.ino).
schematics/: Circuit diagrams (e.g., connection schematic, pinout diagrams).
docs/: Supporting documentation (e.g., test results, project proposal excerpts).
README.md: This file.

**Prerequisites**
**Hardware:**
ESP8266 NodeMCU (ESP-12E module).
4-Channel Relay Module (5V, 10A 250V AC).
230V AC to 5V DC Power Supply.
Appliances (e.g., charger, fan, light).
Manual toggle switch (emergency cutoff).

**Software:**
Arduino IDE (with ESP8266 board support).
Sinric Pro account and API key.
WiFi network with internet access.



**Setup Instructions**

**Hardware Assembly:**

Connect the ESP8266 GPIO pins to the relay module inputs (see schematics/connection_schematic.png).
D1 (GPIO5) → IN1, D2 (GPIO4) → IN2, D5 (GPIO14) → IN3, D6 (GPIO12) → IN4.
Power the ESP8266 and relay module with the 5V DC supply.
Wire the emergency cutoff switch to interrupt the 230V input.
Refer to schematics/pinout_esp8266.png and schematics/pinout_relay.png for pin details.


**Software Configuration:**

Install the Arduino IDE and add ESP8266 board support (via Board Manager).
Install the Sinric Pro library via the Arduino Library Manager.
Open src/main.ino and update the following:
WiFi SSID and password.
Sinric Pro API key (obtain from your Sinric Pro account).
Upload the code to the ESP8266.

**Sinric Pro Setup:**
Register devices (e.g., charger, fan, light) on the Sinric Pro dashboard.
Link the API key to your ESP8266 device.


**Testing:**
Power on the system and connect to WiFi.
Use the Sinric Pro dashboard or voice commands to control devices.
Verify emergency cutoff functionality.

**Usage**
Access the Sinric Pro dashboard (see docs/sinric_pro_screenshot.png) to turn devices on/off.
Use voice commands (e.g., via Alexa/Google Assistant with Sinric Pro integration).
Toggle manual switches for local control.
Monitor status updates on the dashboard.

**Known Issues**
Ensure stable WiFi connectivity; weak signals may cause delays.
Verify 5V power supply output (4.8V - 5.2V) to avoid ESP8266 resets.

**Contributing**
This is an academic project. Contributions are welcome for educational purposes—please fork the repository and submit pull requests with clear descriptions.

**Additional Resources**
Project Proposal: See Appendix A in the project report for initial objectives.
Test Results: Refer to Table 3 in the report for validation data.
Screencast: Watch the demonstration video at [insert link, e.g., https://onedrive.live.com/yoursharedlink] (shared with supervisor and marker).
Contact: For questions, reach out to the project author (anonymized) via GitHub issues.
