# 🌿 IISc Campus Biodiversity Monitoring Network
> **Automated, real-time invasive species detection for the Indian Institute of Science.**

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status: MVP Complete](https://img.shields.io/badge/Status-MVP--Complete-success)
![Hardware: ESP32--S3](https://img.shields.io/badge/Hardware-ESP32--S3-blue)
![Backend: PHP 8.1](https://img.shields.io/badge/Backend-PHP%208.1-777bb4)

---

## 📖 Table of Contents
- [🎯 Project Overview](#-project-overview)
- [🏗️ System Architecture](#️-system-architecture)
- [⚡ Key Features](#-key-features)
- [🛠️ Tech Stack](#️-tech-stack)
- [🚀 Quick Start](#-quick-start)
- [📊 Field Results](#-field-results)
- [👥 Team & Contacts](#-team--contacts)

---

## 🎯 Project Overview
The **IISc Campus Biodiversity Monitoring Network** is a high-fidelity IoT ecosystem designed to protect the local flora and fauna of the IISc campus. By deploying distributed "Smart Traps," we provide the campus administration with a real-time heatmap of invasive species, enabling rapid intervention before ecological damage occurs.

> **Note:** This was developed as a 1-month high-intensity MVP for a BTech Final Year Project.

---

## 🏗️ System Architecture



The system follows a tri-tier architecture:
1.  **The Edge Layer**: ESP32-S3 units capture and transmit geotagged images via 4G/LTE.
2.  **The Cloud Layer**: A PHP-based backend runs TensorFlow Lite models to classify species.
3.  **The Interaction Layer**: A real-time web dashboard and a Flutter-based "Citizen Science" mobile app for community reporting.

---

## ⚡ Key Features

| Feature | Description |
| :--- | :--- |
| **Autonomous Imaging** | 5MP Arducam captures at 30-min intervals. |
| **Edge-to-Cloud** | High-speed LTE (SIM7670G) uploads with fallback logic. |
| **AI Classification** | TFLite model detects 5 specific species with >85% accuracy. |
| **Precision Geofencing** | u-blox NEO-6M provides ±10m location accuracy. |
| **Threat Intelligence** | Auto-escalation (SMS/Email) for **RED-level** detections. |
| **Live Analytics** | Leaflet.js dashboard with interactive heatmaps. |

---

## 🛠️ Tech Stack

### **Hardware**
- **Microcontroller:** ESP32-S3 (Dual-core AI-capable)
- **Modem:** SIM7670G (Global 4G LTE)
- **GNSS:** u-blox NEO-6M GPS
- **Optics:** Arducam 5MP OV5642

### **Software**
- **Inference:** TensorFlow Lite + Python
- **Backend:** PHP 8.1 / MySQL
- **Frontend:** Leaflet.js / Bootstrap 5
- **Mobile:** Flutter (Dart)

---

## 🚀 Quick Start

### 1. Setup Environment
bash
git clone [https://github.com/AerioJobin/IISc-Campus-Biodiversity-Monitoring.git](https://github.com/AerioJobin/IISc-Campus-Biodiversity-Monitoring.git)
cd IISc-Campus-Biodiversity-Monitoring
pip install -r requirements.txt
2. Launch Backend
Bash
cd backend/php
php -S 0.0.0.0:8000
3. Access Dashboard
Navigate to http://localhost:8000/frontend/dashboard/index.html in your browser.

📊 Field Results (72-Hour Test)
Transmission Success: 98.4%

Avg. Latency (Capture to Alert): 4m 12s

GPS Drift: < 4 meters

Battery Consumption: 12% total (5000mAh LiPo)

👥 Team & Contacts
Lead Developer: Aerio Jobin

Institution: Indian Institute of Science (IISc), Bangalore

Contact: [Your Email/LinkedIn]

Last Updated: 2026-03-29 | MIT License


---

# 2. Revamped `PRD.md`

markdown
# 📝 Product Requirements Document (PRD)
## IISc Campus Biodiversity Monitoring Network

| Version | Date | Status | Author |
| :--- | :--- | :--- | :--- |
| 1.0 | 2026-03-29 | ✅ Released | Aerio Jobin |

---

## 1. Executive Summary
This document outlines the technical and functional requirements for an automated biodiversity monitoring network at IISc. The goal is to replace manual, infrequent surveys with high-resolution, real-time data collection to mitigate the impact of invasive species.

---

## 2. Problem Statement
* **Frequency Gap:** Current surveys are conducted only 2–4 times per year.
* **Spatial Blindness:** No data exists for "in-between" zones of the campus.
* **Latency:** Invasive species are often only identified once they have established a colony.

---

## 3. Core Requirements

### 🔵 3.1 Edge Device Requirements
* **Imaging:** 5MP JPEG capture with Q4 compression to balance detail/bandwidth.
* **Network:** Support for 4G LTE-CAT1 for reliable transmission in forested areas.
* **Durability:** IP65-rated housing for monsoon resistance.

### 🟡 3.2 Backend & Intelligence
* **Classification:** TensorFlow Lite inference must take `<2.0s` per image.
* **Prioritization:** * **GREEN:** Native species.
    * **YELLOW:** Non-native, non-invasive.
    * **RED:** Confirmed invasive (Triggers SMS/Email).

### 🟢 3.3 Frontend & Dashboard
* **Real-time:** Map must update via AJAX/WebSockets every 10 seconds.
* **History:** Users must be able to view a 30-day "Time-lapse" of threat movement.

---

## 4. Non-Functional Requirements (NFRs)

> [!IMPORTANT]
> These metrics are the baseline for project success.

| Attribute | Target Metric |
| :--- | :--- |
| **Detection Accuracy** | ≥ 85% for top 5 species |
| **Alert Latency** | < 300 seconds (5 minutes) |
| **Uptime** | 99% during field testing |
| **Battery Life** | 30+ Days (Deep sleep mode) |

---

## 5. User Personas
1.  **Ecologist:** Needs raw data and high-res images for species validation.
2.  **Campus Admin:** Needs the "Heatmap" to deploy removal teams.
3.  **Student:** Uses the Flutter app to report sightings near hostels.

---

## 6. Success Metrics
* **Primary:** Reduction in detection time for invasive species from 3 months (manual) to < 1 day (automated).
* **Secondary:** High engagement on the Mobile Citizen Science app (>100 reports/month).

---
