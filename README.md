# Smart Presence-Based Lighting System

An intelligent **IoT-based automatic lighting system** built using **ESP32**, **PIR motion sensing**, and a **web control dashboard**.  
This project is designed to automate room or office lighting based on human presence while still allowing full manual control through a web interface.

The system automatically turns lights **ON** when someone enters the room and turns them **OFF** when the room becomes empty.  
It also supports **manual override mode**, where lights can be controlled directly from the web dashboard without interrupting automation logic.

This makes the project ideal for **smart homes**, **offices**, **meeting rooms**, **classrooms**, and **energy-saving automation systems**.

---

## 🚀 Project Overview

Traditional lighting systems waste a significant amount of electricity because lights often remain ON even when no one is present.  
This project solves that problem by combining **occupancy detection** with **manual smart control**.

The system continuously monitors room activity using a **PIR sensor**:

- When a person enters the room, motion is detected and the light turns **ON**
- As long as people are present, the system keeps monitoring occupancy
- When everyone leaves the room and no motion is detected for a defined time, the light turns **OFF** automatically

In addition to automatic operation, the project includes a **web dashboard** for manual control:

- Users can manually turn the light **ON** or **OFF**
- If the light is manually turned **ON**, it remains ON regardless of PIR detection
- During manual ON mode, automatic control is temporarily paused
- Once the user manually turns the light **OFF**, the system automatically returns to **Auto Mode**
- Auto Mode resumes and the PIR sensor again controls the light based on room occupancy

This creates a **hybrid smart lighting system** that combines:
- **Automatic occupancy-based control**
- **Manual remote override**
- **Energy efficiency**
- **User flexibility**

---

## ✨ Key Features

- Automatic light control using **PIR motion detection**
- Occupancy-based room automation
- Light turns ON when someone enters
- Light turns OFF when room becomes empty
- Manual ON/OFF control via web dashboard
- Manual override mode
- Automatic return to smart mode after manual OFF
- Real-time control using Wi-Fi
- ESP32-based low-cost smart automation
- Energy-saving and efficient operation

---

## 🧠 System Working Logic

The project works in **two operating modes**:

### 1. Automatic Mode (Default)
This is the default mode of operation.

- The PIR sensor continuously monitors motion
- If motion is detected, the ESP32 turns the light ON
- If no motion is detected for a set timeout, the ESP32 turns the light OFF
- The system keeps running automatically without user intervention

### 2. Manual Override Mode
This mode is activated through the web dashboard.

- User manually turns the light ON from the web app
- The system enters **Manual Override Mode**
- In this mode, PIR sensor automation is paused
- Even if no motion is detected, the light stays ON
- The light remains ON until the user manually turns it OFF
- Once turned OFF manually, the system exits override mode
- The system automatically returns to **Automatic Mode**

This ensures users always have full control when needed without disabling automation permanently.

---

## 🔄 Mode Switching Logic

| Condition | System Behavior |
|----------|------------------|
| Person enters room | Light turns ON automatically |
| Motion detected | Light stays ON |
| Room becomes empty | Light turns OFF automatically |
| User turns light ON from web app | Manual Override Mode enabled |
| No motion during manual ON | Light remains ON |
| User turns light OFF from web app | Manual Override disabled |
| Manual OFF completed | System returns to Auto Mode |

---

## 🛠️ Technologies Used

### Hardware
- ESP32 Development Board
- PIR Motion Sensor
- Relay Module
- AC Light / Load
- Jumper Wires
- Power Supply

### Software
- Arduino IDE
- Embedded C++
- HTML / CSS / JavaScript
- Wi-Fi Communication
- Web Dashboard UI

---

## 📡 How the System Works

1. ESP32 powers ON and connects to Wi-Fi  
2. PIR sensor starts monitoring room movement  
3. If a person enters, motion is detected  
4. ESP32 turns ON the connected light  
5. If motion stops and room becomes empty, light turns OFF  
6. User can manually control light from web dashboard  
7. Manual ON pauses automation  
8. Manual OFF re-enables automatic mode  

---

## 💻 Web Dashboard Features

The project includes a smart web-based control panel that allows users to:

- Monitor light status
- Turn light ON manually
- Turn light OFF manually
- Override automatic mode
- Return system to automatic mode seamlessly

The dashboard provides a simple and responsive interface for both desktop and mobile devices.

---

## ⚡ Benefits of This Project

- Saves electricity
- Reduces human effort
- Prevents unnecessary power consumption
- Adds smart automation to rooms/offices
- Improves user convenience
- Supports both automation and manual control
- Low-cost and easy to deploy

---

## 🏢 Applications

This project can be used in:

- Smart Homes
- Offices
- Cabins
- Meeting Rooms
- Classrooms
- Washrooms
- Corridors
- Conference Rooms
- Smart Buildings

---

## 🔮 Future Improvements

- Add multi-room control
- Add occupancy counting
- Add mobile app support
- Add MQTT / cloud monitoring
- Add voice assistant integration
- Add energy consumption analytics
- Add scheduling features
- Add OTA firmware updates

---

## 👨‍💻 Author

Developed by **Ankit Rajput**  
ESP32 | IoT | Embedded Systems | Smart Automation

---

## ⭐ Support

If you found this project useful:

- Star this repository
- Fork it
- Share it with others
