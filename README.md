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
bash
    git clone https://github.com/AerioJobin/IISc-Campus-Biodiversity-Monitoring.git
    cd IISc-Campus-Biodiversity-Monitoring
    
2. Install Dependencies
    bash
    pip install tensorflow pillow numpy
3. Start Backend
    bash
    cd backend/php
    php -S 0.0.0.0:8000
4. View Dashboard
    Open: http://localhost:8000/frontend/dashboard/index.html

###Project structure
IISc-Campus-Biodiversity-Monitoring/
├── README.md
├── PRD.md
├── MVP_PLAN.md
├── FIELD_RESULTS.md
├── DIFFERENTIATION.md
├── FUTURE_ROADMAP.md
├── LICENSE
├── CONTRIBUTING.md
├── .gitignore
├── docs/
├── backend/
├── frontend/
├── firmware/
├── mobile/
├── tests/
└── deployment/

📚 Documentation
Document	Purpose
PRD.md	Product Requirements
MVP_PLAN.md	1-month execution timeline
FIELD_RESULTS.md	72-hour deployment outcomes
DIFFERENTIATION.md	vs Western Sydney comparison
FUTURE_ROADMAP.md	Phases 2-4 plans
👥 Team & Contacts
Project Lead: Aerio Jobin
GitHub: https://github.com/AerioJobin/IISc-Campus-Biodiversity-Monitoring
Institution: Indian Institute of Science (IISc), Bangalore
📜 License
MIT License - see LICENSE file.

Last Updated: 2026-03-29
Status: 🚀 MVP Complete & Field Tested

Code

4. Click **"Commit changes"**
5. Write message: `Add comprehensive README.md`
6. Click **"Commit directly to main branch"**

---

#### **Step 3: Create PRD.md**
1. Click **"Add file"** → **"Create new file"**
2. Name: `PRD.md`
3. Paste:

```markdown
# 📝 Product Requirements Document (PRD)

**IISc Campus Biodiversity Monitoring Network**

**Version**: 1.0  
**Date**: 2026-03-29  
**Author**: Aerio Jobin

---

## 1. Executive Summary

The **IISc Campus Biodiversity Monitoring Network** is an IoT-based, real-time system for detecting invasive insect species within the IISc campus ecosystem.

---

## 2. Problem Statement

- Manual biodiversity surveys at IISc are **infrequent** (2-4 times/year)
- Survey data **lacks spatial resolution**
- Invasive species detected **days after arrival** (too late!)
- **No automated monitoring** exists

---

## 3. Functional Requirements

### Edge Devices
- ✅ 5MP JPEG image capture via Arducam
- ✅ JPEG Q4 compression
- ✅ 15–30 min capture interval
- ✅ GPS tagging (≤10m accuracy)
- ✅ Battery voltage telemetry
- ✅ 4G/LTE connectivity via SIM7670G

### Backend
- ✅ PHP receiver for multipart form data
- ✅ TensorFlow Lite inference (<2 sec/image)
- ✅ 5 species classification (4 invasive + 1 native)
- ✅ Threat levels: GREEN / YELLOW / RED
- ✅ SMS/Email alerts for RED threats
- ✅ ≥99% uptime

### Dashboard
- ✅ Leaflet.js live map
- ✅ Image gallery + threat heatmap
- ✅ Real-time alert panel
- ✅ 10-sec auto-refresh
- ✅ Mobile responsive

### Mobile App
- ✅ Photo upload + geotag
- ✅ Species guess + notes
- ✅ Push notifications
- ✅ User profile & stats

---

## 4. Non-Functional Requirements

| Requirement | Target |
|------------|--------|
| **Accuracy** | ≥85% species detection |
| **Alert Latency** | <5 min image→SMS |
| **Uptime** | ≥99% |
| **GPS Accuracy** | ≤10m |
| **Battery Life** | ≥30 days field |
| **False Alert Rate** | <10%/week |

---

## 5. Project Phases

1. **Phase 1 (Weeks 1-2)**: Hardware & Firmware
2. **Phase 2 (Weeks 2-3)**: Backend & ML
3. **Phase 3 (Week 3)**: Frontend & Alerts
4. **Phase 4 (Week 3-4)**: Mobile App
5. **Phase 5 (Week 4)**: Field Test & Validation

---

## 6. Success Metrics

- ✅ Detection Accuracy: ≥85%
- ✅ Alert Latency: <5 min
- ✅ Uptime: ≥99%
- ✅ Zero Data Loss: 100% image transmission

---

## 7. Stakeholders

- **IISc Ecology Lab**: Species validation
- **Campus Admin**: Infrastructure support
- **Students**: Citizen science participation
- **Developer**: Aerio Jobin

---

**Document Status**: ✅ Complete
