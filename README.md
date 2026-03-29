# 🌿 IISc Campus Biodiversity Monitoring Network

**An automated, hyperlocal, real-time invasive species detection and biodiversity monitoring system for the Indian Institute of Science campus.**

---

## 📋 Table of Contents

- [Project Overview](#-project-overview)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Quick Start](#-quick-start)
- [Documentation](#-documentation)
- [Team & Contacts](#-team--contacts)

---

## 🎯 Project Overview

**IISc Campus Biodiversity Monitoring Network** is a **1-month MVP (Minimum Viable Product)** developed as a BTech final year project. It demonstrates the feasibility of automated, distributed invasive species detection using:

- **IoT Trap Units**: ESP32-S3 microcontroller with 5MP camera, GPS, LTE modem
- **Cloud Backend**: PHP API with local TensorFlow Lite inference for species classification
- **Real-Time Alerts**: SMS/Email for invasive species detection (RED threat level)
- **Web Dashboard**: Live Leaflet.js map with trap locations, image gallery, and threat heatmap
- **Mobile App**: Flutter citizen science app for campus community participation
- **Field Validation**: 72-hour deployment with GPS accuracy and battery endurance testing

---

## ⚡ Key Features

✅ Autonomous Imaging: ESP32-S3 captures 5MP images every 30 min  
✅ 4G Connectivity: SIM7670G uploads via LTE to cloud backend  
✅ GPS Tracking: u-blox NEO-6M provides ±10m accuracy  
✅ AI Classification: TensorFlow Lite model detects 5 species  
✅ Real-Time Alerts: SMS/Email sent <5 min for RED-level detections  
✅ Live Dashboard: Leaflet.js map + image gallery + threat analytics  
✅ Mobile App: Flutter app for citizen sightings  
✅ Field Tested: 72-hour continuous deployment with validation  
✅ 100% Documented: All code, processes, and decisions logged  
✅ Open Source: MIT License, ready for community contribution  

---

## 🏗️ Tech Stack

| Component | Technology |
|-----------|-----------|
| Edge Device | ESP32-S3 + Arducam 5MP + SIM7670G |
| Backend | PHP 8.1 + MySQL |
| ML Inference | TensorFlow Lite + Python 3 |
| Frontend | Leaflet.js + HTML5/CSS3/JS |
| Mobile | Flutter (Dart) |
| Alerts | Twilio / AWS SNS |

---

## 🚀 Quick Start

### 1. Clone Repository
```bash
git clone https://github.com/AerioJobin/IISc-Campus-Biodiversity-Monitoring.git
cd IISc-Campus-Biodiversity-Monitoring
