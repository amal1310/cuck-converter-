# Smart Battery Charger Using CUK Converter and CT2000 Controller

## 📖 Project Overview

This project implements a high-efficiency **CUK Converter Based Smart Battery Charger** designed to convert **30V DC input** into a regulated charging voltage for a **4S Lithium-Ion Battery Pack**.

The system uses a **CT2000 Controller** for PWM generation, voltage regulation, charging control, protection mechanisms, and battery balancing. Additional sensors monitor voltage, current, and temperature to ensure safe operation.

---

## 🎯 Objectives

- Convert 30V DC input to regulated battery charging voltage.
- Charge a 4S Lithium-Ion battery safely and efficiently.
- Monitor battery voltage, current, and temperature.
- Implement battery balancing functionality.
- Protect against over-voltage, over-current, and over-temperature conditions.
- Improve converter efficiency and battery life.

---

## ⚡ System Specifications

| Parameter | Value |
|------------|---------|
| Input Voltage | 30V DC |
| Battery Type | 4S Lithium-Ion |
| Nominal Battery Voltage | 14.8V |
| Full Charge Voltage | 16.8V |
| Battery Capacity | 3500mAh |
| Switching Frequency | 20kHz – 50kHz |
| Converter Topology | CUK Converter |
| Controller | CT2000 |

---

## 🔧 Hardware Components

### Power Stage

| Component | Value |
|------------|--------|
| MOSFET | IRF540N |
| Gate Driver | TLP350 |
| Schottky Diode | SR10100CT |
| Fast Recovery Diode | MUR2040 |
| Input Capacitor | 330µF / 50V |
| Transfer Capacitor | 22µF Film Capacitor |
| Output Capacitor | 440µF + 440µF |
| Bypass Capacitor | 0.1µF Polyester |
| Input Inductor (L1) | 92µH |
| Output Inductor (L2) | 75µH |

---

## 🎛 Controller

### CT2000 Controller Functions

- PWM Generation
- Voltage Regulation
- Charging Algorithm
- Battery Monitoring
- Cell Balancing Control
- Fault Detection
- System Protection

---

## 📊 Sensors Used

### ACS712 Current Sensor

Measures:
- Charging Current
- Output Current

### Voltage Sensor

Measures:
- Battery Voltage
- Converter Output Voltage

### LM35 Temperature Sensor

Measures:
- MOSFET Temperature
- Converter Temperature

---

## 🔋 Battery Pack Details

### Configuration

4S1P Lithium-Ion Battery Pack

### Cell Specifications

| Parameter | Value |
|------------|---------|
| Cell Voltage | 3.7V |
| Full Charge Voltage | 4.2V |
| Number of Cells | 4 |
| Capacity | 3500mAh |

### Pack Voltage

| State | Voltage |
|---------|----------|
| Nominal | 14.8V |
| Fully Charged | 16.8V |

---

## ⚖ Battery Balancing

The balancing system ensures all cells maintain equal voltage during charging.

### Benefits

- Increased battery life
- Improved safety
- Better charging efficiency
- Reduced cell stress
- Prevents overcharging of individual cells

### Balancing Features

- Individual cell monitoring
- Voltage equalization
- Cell protection
- Charge optimization

---

## ⚙ Converter Operation

### MOSFET ON State

- Input inductor stores energy.
- Transfer capacitor charges.
- Current increases through L1.

### MOSFET OFF State

- Stored energy transfers to output.
- Output inductor supplies load current.
- Battery receives charging current.

---

## 🛡 Protection Features

### Over Voltage Protection

```text
Output Voltage > Safe Limit
```

### Over Current Protection

```text
Charging Current > Rated Limit
```

### Over Temperature Protection

```text
Temperature > Safe Operating Range
```

### Short Circuit Protection

```text
Output Short Circuit Detection
```

---

## 🧪 Testing Parameters

The following parameters were tested:

- Input Voltage
- Output Voltage
- Battery Voltage
- Charging Current
- Temperature
- PWM Duty Cycle
- Converter Efficiency

### Tested Switching Frequencies

- 20kHz
- 30kHz
- 35kHz
- 40kHz
- 45kHz
- 50kHz

---

## 📁 Project Structure

```text
Smart-CUK-Battery-Charger/
│
├── README.md
├── Hardware/
│   ├── Circuit_Diagram/
│   ├── PCB_Layout/
│   ├── Component_List/
│   └── Datasheets/
│
├── Firmware/
│   ├── CT2000_Control/
│   ├── PWM_Generation/
│   ├── Battery_Monitoring/
│   └── Protection_System/
│
├── Documentation/
│   ├── Project_Report.pdf
│   ├── Testing_Results.pdf
│   └── Design_Calculations.pdf
│
├── Images/
│   ├── Hardware_Setup.jpg
│   ├── Circuit_Diagram.png
│   ├── PCB_Layout.png
│   └── Waveforms.png
│
└── Results/
    ├── Efficiency_Data.xlsx
    └── Test_Logs.csv
```

---

## 🚀 Future Enhancements

- MPPT Solar Charging
- IoT Monitoring
- WiFi Connectivity
- Mobile Application
- OLED Display
- Cloud Data Logging
- AI-Based Battery Health Prediction
- Remaining Useful Life (RUL) Estimation

---

## 🎓 Applications

- EV Battery Charging
- Solar Energy Storage Systems
- UPS Battery Systems
- Portable Power Stations
- Industrial Battery Chargers
- Smart Energy Management Systems

---

## 👨‍💻 Author

**Amal M**

Embedded Systems Engineer | AI Engineer

### Areas of Interest

- Embedded Systems
- Power Electronics
- Battery Management Systems (BMS)
- Internet of Things (IoT)
- Artificial Intelligence
- Edge AI
- Data Science

---

## 📜 License

This project is intended for educational, research, and prototype development purposes.

Copyright (c) 2026 Amal M
