# AI-Driven Campus Surveillance & Automated LMS Disciplinary System

An integrated smart campus monitoring and disciplinary management platform that combines computer vision-based behavior detection with a web-based Learning Management System (LMS) to enforce campus policies, generate real-time admin alerts, and automate student warnings with verifiable proof.

## 🏗️ System Architecture & Workflow

The platform is divided into two core synchronized modules located within this repository:

1. **COGNITIVE VISION AI (Detection Engine):** 
   - Continuously processes live video feeds or campus IP camera streams using **YOLOv8** and **OpenCV**.
   - Detects real-time policy violations (such as smoking or vaping).
   - Instantly captures snapshot evidence upon a positive violation trigger and pushes alerts to the backend.

2. **LMS (Web Portal & Disciplinary Management):**
   - Receives real-time alerts on the admin dashboard.
   - Allows administrators to review violation logs along with the attached image proof.
   - Automatically or manually dispatches official warnings directly to the student's portal and registered email address.
   - Provides a student challenge module enabling students to review and formally contest disciplinary flags.

---

## 📂 Repository Structure

```text
AI Hackathon/
│
├── COGNITIVE VISION AI/       # Computer Vision module (YOLOv8, inference scripts, model weights)
│   ├── models/                # Trained YOLOv8 detection weights (e.g., smoking.pt)
│   ├── inference.py           # Main real-time video processing script
│   └── requirements.txt       # Python dependencies
│
└── LMS/                       # Web portal and backend management system
    ├── backend/               # Server-side APIs, database connection, alert routes
    ├── frontend/              # Admin dashboard & student portal UI
    └── package.json           # Node.js dependencies
