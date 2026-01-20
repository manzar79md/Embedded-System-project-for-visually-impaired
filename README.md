
---

# 📱 Wrist-Worn Obstacle Detection System for Visually Impaired

A compact, wearable IoT device that assists visually impaired individuals in navigating safely by detecting obstacles in real-time using ultrasonic sensors.

## 🎯 Overview

The device uses an HC-SR04 ultrasonic sensor to detect obstacles within 400cm range and provides dual feedback:
- **Vibration Motor** - Tactile feedback alerts
- **Buzzer** - Auditory feedback alerts

Feedback intensity adapts based on obstacle proximity for optimal user experience.

## ✨ Key Features

✅ Real-time obstacle detection (HC-SR04 ultrasonic sensor)  
✅ Dual feedback system (vibration + buzzer)  
✅ Adaptive alert intensity based on distance  
✅ Compact wrist-worn design for portability  
✅ Rechargeable battery for extended usage  
✅ Fail-safe mechanisms to reduce false alarms  
✅ Easy on/off switch interface  

## 🛠️ Hardware Components

- **Microcontroller**: Arduino/ESP32
- **Sensor**: HC-SR04 Ultrasonic Sensor (0-400cm range)
- **Output Devices**: Vibration Motor + Buzzer
- **Power**: Rechargeable Battery
- **Switch**: Power on/off control

## 💻 Software

- **Language**: C++
- **Platform**: Arduino IDE
- **Key Functions**:
  - `getDistance()` - Measures obstacle distance
  - `activateFeedback()` - Controls vibration/buzzer based on proximity
  - `powerManagement()` - Optimizes battery usage

## 📖 How It Works

1. **Detection**: Ultrasonic sensor continuously scans for obstacles
2. **Analysis**: Distance is calculated using echo time
3. **Feedback**: 
   - Distance < 50cm → Strong vibration + loud buzzer
   - Distance 50-100cm → Medium vibration + medium tone
   - Distance > 100cm → Light vibration + low tone
4. **Safety**: Fail-safe mechanisms prevent rapid false alerts

## 🚀 Setup Instructions

### Hardware Assembly
1. Connect HC-SR04 sensor to trigger and echo pins
2. Connect buzzer to pin 15, vibration motor to pin 16
3. Connect battery through power switch
4. Mount components in wrist-worn enclosure

### Software Upload
```bash
1. Open Arduino IDE
2. Load the obstacle detection code
3. Select Board: ESP32 or Arduino
4. Upload to microcontroller
5. Test with serial monitor
```

### Configuration
- **Trigger Pin**: 12
- **Echo Pin**: 14
- **Buzzer Pin**: 15
- **LED/Vibration Pin**: 16
- **Detection Threshold**: <50cm

## 📊 Performance

- **Obstacle Detection Range**: 0-400cm
- **Accuracy**: ±3cm
- **Response Time**: <500ms
- **Battery Life**: 8-12 hours (continuous use)

## 🔗 Interactive Demo

View live simulation: [Wokwi Project](https://wokwi.com/projects/406034869275608065)

## 🎯 Real-World Applications

- Navigation aid for visually impaired individuals
- Mobility support in indoor/outdoor environments
- Safety enhancement during movement
- Companion device for independent living

## 🔮 Future Enhancements

- Advanced sensors (LIDAR) for improved accuracy
- Wireless connectivity (Bluetooth/WiFi)
- Mobile app integration for real-time monitoring
- Machine learning for pattern recognition
- GPS integration for location tracking

## 📝 License

Open-source project. Free for non-commercial use.

---
