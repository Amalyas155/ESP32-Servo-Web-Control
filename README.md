
# 🤖 ESP32 Servo Web Control

A smart embedded systems project that controls a servo motor through a simple Wi-Fi web interface using an ESP32.

The ESP32 creates its own Wi-Fi Access Point, allowing the user to control the servo motor from a web page without an external router. Red and blue LEDs are used as visual status indicators.

## ✨ Project Features

- 📶 ESP32 works as a Wi-Fi Access Point.
- 🌐 Simple web page with **Open** and **Close** buttons.
- ⚙️ Servo motor control through the web interface.
- 🔵 Blue LED indicates the **Open** state.
- 🔴 Red LED indicates the **Close** state.
- 🧪 Wokwi simulation for circuit and code testing.
- 🚫 No external Wi-Fi router is required.

## ⚙️ System Behavior

| Action | Servo Position | Blue LED | Red LED |
|---|---:|:---:|:---:|
| Open | 90° | ON 🔵 | OFF |
| Close | 0° | OFF | ON 🔴 |

## 🧩 Components Used

- ESP32 DevKit V1
- Servo Motor
- Blue LED
- Red LED
- 2 × 220Ω Resistors
- Jumper Wires

## 🔌 Wiring Connections

| Component | ESP32 Connection |
|---|---|
| Servo PWM | GPIO 18 |
| Servo V+ | 5V |
| Servo GND | GND |
| Blue LED Anode | GPIO 26 through a 220Ω resistor |
| Red LED Anode | GPIO 27 through a 220Ω resistor |
| Both LED Cathodes | GND |

## 🛠️ Software and Libraries

- Arduino C++
- `WiFi.h`
- `WebServer.h`
- `ESP32Servo.h`
- Wokwi Simulator

## 🎥 Project Demo

The following video demonstrates the project running in the Wokwi simulator, including the ESP32 Access Point, web server startup, servo motor movement, and LED status indicators.

https://github.com/user-attachments/assets/0dab219f-925f-41a5-994e-55c59191abb0


## 🌐 Wokwi Simulation

https://wokwi.com/projects/471183592177360897

## 🧪 Testing in Wokwi

1. ▶️ Start the simulation.
2. 💻 Open the Serial Monitor.
3. ✅ Confirm that the Access Point and Web Server start successfully.
4. Type `O` and press Enter to test the **Open** action.
5. Type `C` and press Enter to test the **Close** action.

> 💡 The serial commands are used to test the servo and LEDs in Wokwi.  
> On the physical ESP32, the system is controlled through the web page.

## 📱 Physical ESP32 Setup

1. Upload `sketch.ino` to the ESP32.
2. Connect a phone to the Wi-Fi network below.
3. Open a browser and enter the IP address.

| Setting | Value |
|---|---|
| 📶 Wi-Fi Name | `ESP32-Servo` |
| 🔐 Password | `12345678` |
| 🌐 Web Page Address | `192.168.4.1` |

## 📁 Project Files

```text
ESP32-Servo-Web-Control/
│
├── sketch.ino
├── diagram.json
├── libraries.txt
├── demo.mp4
└── README.md
