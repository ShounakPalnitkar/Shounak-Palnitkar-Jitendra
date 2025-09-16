An Intelligent IoT Navigation System for Visually Impaired Individuals: Design and Implementation


**An advanced wearable assistive technology system designed to improve mobility and independence for visually impaired users.** This project was presented at IEEE AIIOT 2025.

---

## Abstract

The Smart Hat is a holistic wearable system that integrates **voice-guided navigation, real-time object detection, ultrasonic obstacle sensing, and contextual feedback** to enable safe and independent movement. Built on a **Raspberry Pi 5** platform with edge computing capabilities, the system ensures low-latency processing while utilizing secure cloud services (**Firebase, Google Cloud Platform**) for data storage, analysis, and remote monitoring.

---

## Key Features

| Feature | Description | Benefit |
| :--- | :--- | :--- |
| **Real-Time AI Vision** | MobileNetV2 SSD model for detecting objects like people, cars, and chairs. | Provides environmental awareness beyond the reach of a white cane. |
| **360° Obstacle Sensing** | Array of six ultrasonic sensors (HC-SR04) with Kalman filtering. | Detects proximal obstacles from all directions, even in total darkness. |
| **Voice-Guided Feedback** | Integration with Web Speech API for responsive audio cues via smartphone. | Offers clear, timely spoken instructions like *"Obstacle to your left."* |
| **Edge Computing** | On-device processing on Raspberry Pi 5 for low latency (~230ms). | Ensures real-time responsiveness without relying on a cloud connection. |
| **Cloud Dashboard** | Real-time web dashboard (Flask & Plotly Dash) for remote monitoring by caregivers. | Provides peace of mind and allows for remote support and system analysis. |
| **Low-Light Capable** | IR-assisted camera module for improved performance in dim environments. | Maintains functionality during evening or indoor use. |

---

## System Architecture & Tech Stack

The system is built on a modular, three-layer architecture:

### 1. Wearable Device Layer (Hardware)
- **Core Compute:** Raspberry Pi 5
- **Vision:** Sony IMX219 Camera Module (8MP, 160° FOV)
- **Sensing:** 6x HC-SR04 Ultrasonic Sensors
- **Power:** 10000mAh USB-C Power Bank
- **Cooling:** Heatsink & Fan Assembly

### 2. Edge Processing Layer (Software)
- **OS:** Raspberry Pi OS
- **Language:** Python
- **ML Framework:** TensorFlow Lite
- **ML Model:** MobileNetV2 SSD (trained on COCO dataset)
- **Real-Time Communication:** WebSocket (Socket.IO)

### 3. Cloud & Interface Layer
- **Database & Storage:** Google Firebase (Firestore, Storage)
- **Web Server:** Flask (Python)
- **Web Dashboard:** Plotly Dash, HTML5, JavaScript
- **Text-to-Speech:** Web Speech API
- **Tunneling:** Ngrok (for secure remote access)



---

## Performance & Results

Experimental validation demonstrated robust performance across diverse environments:

| Metric | Result |
| :--- | :--- |
| **Object Detection Accuracy** | >83% on common classes (person, car, chair) |
| **Directional Localization Accuracy** | >95% |
| **End-to-End System Latency** | 230 - 260 ms |
| **Battery Life** | ~2.5 - 3 hours (with 10000mAh battery) |
| **CPU Usage (Avg.)** | 38.4% |
| **Memory Usage (Avg.)** | 18.7% |
| **Operating Temperature (Avg.)** | 87.1°C (Active cooling required) |

*Results were achieved primarily in daylight conditions. A 40% reduction in collisions was observed in user trials.*

---

## Repository Contents

This repository serves as the documentation and project showcase for the Smart Hat system. It contains:
- This comprehensive `README.md`
- **`/images`** directory: Contains system diagrams, hardware photos, and result charts.
- **`/docs`** directory: Contains the published paper and presentation slides.
- **`LICENSE`** file: MIT License.

*Note: The source code is not included in this repository as it is part of an ongoing academic research project.*

---

## Future Work

- **Thermal & Power Management:** Implementation of low-power processors and advanced cooling solutions to address high operating temperatures and limited battery life.
- **Enhanced Navigation:** Integration of IMU sensors and UWB for reliable indoor positioning.
- **Low-Light Algorithms:** Development of improved detection models for challenging lighting conditions.
- **Dedicated Mobile App:** Development of an offline-ready Android application for improved reliability and user experience.

---

## Authors

- **Punam Ram Pukale** - Department of Computer Science, University of the Pacific
- **Kushal Sri Rangan** - Department of Computer Science, University of the Pacific
- **Shounak Palnitkar Jitendra** - Department of Computer Science, University of the Pacific
- **Dongbin Lee*** - Department of Computer Engineering, University of the Pacific
- **Jinzhu Gao** - Department of Computer Science, University of the Pacific

---

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.

---

## Citation

If you find our work useful for your research, please consider citing our paper:

```bibtex
@article{pukale2025intelligent,
  title={An Intelligent IoT Navigation System for Visually Impaired Individuals: Design and Implementation},
  author={Pukale, Punam Ram and Rangan, Kushal Sri and Jitendra, Shounak Palnitkar and Lee, Dongbin and Gao, Jinzhu},
  journal={IEEE AIIOT},
  year={2025}
}
