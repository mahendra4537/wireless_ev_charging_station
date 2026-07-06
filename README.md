# 🚗 Wireless EV Charging Station with RFID Authentication

A smart IoT-based Wireless Electric Vehicle Charging Station developed using ESP32, RFID authentication, Firebase Realtime Database, and a live web dashboard.

This project demonstrates a prototype charging station where only authorized users can access the charging area. The system provides real-time charging information through a web interface and simulates EV charging parameters.

---

## 📌 Features

- 🔐 RFID-based user authentication
- 🚗 Automatic gate control using SG90 servo motor
- 🔊 Buzzer notification for access status
- 📟 16x2 I2C LCD for user messages
- 🌐 Wi-Fi connectivity using ESP32
- ☁ Firebase Realtime Database integration
- 📊 Live web dashboard
- 🔋 Battery charging simulation
- ⚡ Charging speed monitoring
- ⏳ Estimated charging time calculation
- 📱 Responsive dashboard accessible from any device

---

## 🛠 Hardware Used

| Component | Quantity |
|------------|----------|
| ESP32 DevKit V1 | 1 |
| RC522 RFID Reader | 1 |
| RFID Card | 1 |
| SG90 Servo Motor | 1 |
| 16x2 I2C LCD Display | 1 |
| Active Buzzer | 1 |
| Breadboard | 1 |
| Jumper Wires | As Required |
| USB Cable | 1 |

---

## 🔌 Pin Connections

| ESP32 Pin | Component |
|------------|-----------|
| GPIO13 | Servo Signal |
| GPIO5 | RFID SDA |
| GPIO18 | RFID SCK |
| GPIO19 | RFID MISO |
| GPIO23 | RFID MOSI |
| GPIO27 | RFID RST |
| GPIO21 | LCD SDA |
| GPIO22 | LCD SCL |
| GPIO25 | Buzzer |

---

## ⚙ Working Principle

1. User scans an RFID card.
2. The ESP32 verifies the UID.
3. If the card is authorized:
   - LCD displays **Access Granted**
   - Servo opens the gate (90°)
   - After 2 seconds, the gate closes
   - Buzzer sounds for 2 seconds
   - Charging session starts
4. Charging data is uploaded to Firebase Realtime Database.
5. The web dashboard automatically updates in real time.
6. Battery percentage increases until fully charged.

---

## 📊 Web Dashboard Displays

- Charging Status
- Battery Percentage
- Charging Speed
- Estimated Remaining Time
- Vehicle Number
- RFID User
- Gate Status
- Last Scan Information
- Live Battery Progress Bar

---

## ☁ Firebase Realtime Database

Example Database Structure

```json
station
{
  "user":"Ashok",
  "vehicle":"AP39AB1234",
  "battery":65,
  "chargingSpeed":"7.2 kW",
  "estimatedTime":"1 hr 15 min",
  "status":"Charging",
  "gate":"Closed",
  "lastScan":"BD D5 F7 04"
}
```

---

## 💻 Technologies Used

### Embedded

- Arduino IDE
- ESP32
- C++

### IoT

- Firebase Realtime Database
- Wi-Fi Communication

### Web

- HTML5
- CSS3
- JavaScript
- Firebase Web SDK

---

## 📂 Project Structure

```
Wireless-EV-Charging-Station/
│
├── ESP32/
│   └── EV_Charging_Station.ino
│
├── Web/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── Images/
│
└── README.md
```

---

## 📈 Future Improvements

- User login system
- Multiple RFID users
- QR code authentication
- Online payment integration
- Mobile application
- Real battery voltage monitoring
- Charging history
- Admin dashboard
- Slot reservation system
- Email/SMS notifications

---

## 🎯 Applications

- Smart EV Charging Stations
- College Mini Projects
- IoT Demonstrations
- Smart Parking Systems
- RFID Access Control Systems
- Renewable Energy Projects

---

## 📷 Project Images

Add screenshots here.

- Hardware Setup
- Web Dashboard
- Firebase Database
- Circuit Diagram

---

## 📹 Demo

Add your project demonstration video or YouTube link here.

---

## 🚀 Getting Started

1. Clone this repository.
2. Open the ESP32 project in Arduino IDE.
3. Configure your Wi-Fi credentials.
4. Configure Firebase.
5. Upload the code to ESP32.
6. Open the web dashboard.
7. Scan the authorized RFID card.

---

## 📜 License

This project is developed for educational and learning purposes.

---

## 👨‍💻 Author

**mahendra**

Electronics & Communication Engineering Student

Wireless EV Charging Station using ESP32, RFID, Firebase, and Web Dashboard.
