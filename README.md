# Classroom Automation System 💡⚡

**A smart classroom automation solution using `NodeMCU`, `Firebase Realtime Database`, and `MIT App Inventor` for remote and automated control of lights and fans.**

[![Status](https://img.shields.io/badge/status-complete-success.svg)]() 
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

<br>

> The system is designed to improve energy efficiency, enhance convenience for educators and students, and provide secure, remote access to classroom appliances.

<br>



---

## 📌 Core Features

* **📱 Remote Control:** Seamlessly switch lights and fans ON/OFF directly from a custom-built mobile application.
* **🔐 Secure Login Authentication:** Ensures that only authorized users can access the control panel via a secure app login.
* **🔄 Real-time Sync:** Leverages **Firebase Realtime Database** for instantaneous updates between the mobile app and the NodeMCU hardware.
* **🤖 Smart Automation Mode:**
    * Controls appliances intelligently based on **room occupancy** detected by a PIR sensor.
    * Adjusts fan operation automatically according to the **ambient room temperature**.
* **💸 Significant Energy Savings:** Designed to achieve an estimated **25–30% reduction** in energy consumption by eliminating wastage.

---

## 🛠️ Tech Stack

### Hardware
* **Microcontroller:** NodeMCU ESP8266
* **Sensors:** * DHT11 Temperature & Humidity Sensor
    * PIR Motion Sensor (for occupancy detection)
* **Actuators:** Relay Modules (for controlling 220V lights and fans)
* **Power:** 5V Power Supply Unit

### Software & Cloud
* **Firmware Development:** Arduino IDE
 **Database:** Firebase
* **Mobile App:** MIT App Inventor

---

## ⚙️ How It Works

The system operates in a closed loop, ensuring seamless communication between the hardware, cloud, and the user app.

**User App** ⇄ **Firebase Realtime Database** ⇄ **NodeMCU** ⇄ **Classroom Appliances**

1.  **Sensor Data Collection:** The **PIR sensor** detects movement (occupancy) and the **DHT11 sensor** measures the current temperature.
2.  **Data Sync to Cloud:** The NodeMCU reads this sensor data and continuously updates it to the Firebase Realtime Database.
3.  **App Interaction:** The mobile app fetches real-time sensor data from Firebase and displays it. The user can use control switches in the app to send commands back to Firebase.
4.  **Hardware Control:** The NodeMCU listens for changes in the database. When a command is received (e.g., "Turn Light ON"), it triggers the corresponding relay module to control the appliance.
5.  **Automation Logic:**
    * If no occupancy is detected for a set period, the NodeMCU automatically turns OFF all lights and fans.
    * If the temperature rises above a predefined threshold, the fan is automatically switched ON.

---

### 📂 Project Structure

```bash
Classroom-Automation/
├── arduino_code/main/        # NodeMCU Arduino main code
├── firebase-setup/           # Images of Real-time Database structure
├── images/                   # Circuit diagrams and project photos
├── laser-cutting-stencil/    # SVG Stencil for the Laser-Cut project box
├── mobile-app-setup-mit/     # Screenshots of MIT App Inventor blocks
└── README.md

---

## 🔌 Circuit Diagram

The circuit connects the NodeMCU with the DHT11 sensor, PIR sensor, and relay modules for controlling standard classroom appliances.

<img width="752" height="895" alt="image" src="https://github.com/user-attachments/assets/fbfe0f11-732c-4032-9bb5-d02773cb2f85" />


---

## 📈 Future Improvements

-   [ ] **Voice Control:** Integration with voice assistants like Google Assistant or Amazon Alexa.
-   [ ] **Data Analytics:** A cloud-based dashboard for visualizing energy usage patterns over time.
-   [ ] **Sustainability:** Integration with solar power to make the system even more eco-friendly.

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

**Chetan Chauhan**
