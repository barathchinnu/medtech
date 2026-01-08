# 🚑 Smart Emergency Medical Response System

A **software-based emergency healthcare platform** designed to reduce response time during medical emergencies by connecting **patients, ambulance drivers, and hospitals** through a real-time, Uber-style workflow.

---
## Problem Statement
In emergency medical situations, delays often occur due to lack of coordination between patients, ambulance services, and hospitals. Manual communication and absence of real-time systems lead to increased response time, which can result in loss of life.

---

## Objective
- To reduce emergency response time  
- To provide real-time ambulance assignment  
- To notify hospitals in advance based on emergency type  
- To improve coordination between patients, drivers, and hospitals  

## ✨ Features

- **Emergency Request System**
  - One-tap emergency button
  - Emergency type selection (Accident, Heart Disease, Pregnancy, etc.)

- **Live Location Tracking**
  - Automatically captures patient GPS location
  - Enables navigation for ambulance drivers

- **Ambulance Driver Portal (Uber-like)**
  - View nearby emergency requests
  - Accept or reject requests in real time

- **Hospital Coordination**
  - Hospitals receive emergency alerts
  - Acceptance based on doctor availability

- **Real-Time Status Updates**
  - Request created → Accepted → Patient picked → Hospital reached

- **Responsive Design**
  - Works on desktop and mobile browsers

---

## 🛠 Tech Stack

- **Frontend**: React.js, HTML5, CSS3, JavaScript, Vite  
- **Backend**: Java 17, Spring Boot, Maven  
- **Database**: MySQL  
- **APIs**: RESTful APIs  
- **Maps & Location**: Google Maps API  

---

## 🔄 Workflow – How It Works

1. **Landing Page**
   - Displays emergency button
   - User grants location permission

2. **Emergency Selection**
   - Patient selects type of emergency
   - Live location is captured

3. **Request Creation**
   - Emergency request sent to backend
   - Stored in MySQL database

4. **Ambulance Notification**
   - Nearby ambulance drivers receive alerts
   - Driver accepts the request

5. **Patient Pickup**
   - Driver navigates to patient location
   - Status updated in real time

6. **Hospital Notification**
   - Emergency details sent to hospitals
   - Hospital accepts based on doctor availability

7. **Hospital Navigation**
   - Ambulance navigates to accepted hospital

---

## 🏗 Architecture

### High-Level Flow

- **Frontend (React.js)**
  - User interface for patients, drivers, and hospitals
  - Sends and receives real-time updates

- **Backend (Spring Boot)**
  - Handles emergency requests
  - Assigns ambulances
  - Notifies hospitals

- **Database (MySQL)**
  - Stores users, emergencies, ambulance, and hospital data

### Architecture Diagram

[ Patient Browser ]
|
v
[ Frontend (React) ]
|
v
[ Backend (Spring Boot) ]
|
v
[ MySQL Database ]

Save the diagram as `docs/architecture.png` and embed it using:
```md
![Architecture Diagram](docs/architecture.png)
🚀 Quick Start
Local Development
Backend
bash
Copy code
cd medical-response-backend
mvn spring-boot:run
Backend runs at:

arduino
Copy code
http://localhost:8080
Frontend
bash
Copy code
cd MedicalResponseApp
npm install
npm run dev
Frontend runs at:

arduino
Copy code
http://localhost:5173
🔗 API Endpoints
Method	Endpoint	Description
POST	/api/emergency	Create emergency request
GET	/api/emergency/nearby	Fetch nearby emergencies
POST	/api/driver/accept	Driver accepts request
POST	/api/hospital/accept	Hospital accepts emergency
GET	/api/emergency/{id}	View request status

📂 Project Structure
css
Copy code
medical-response-system/
├── medical-response-backend/
│   ├── src/main/java/
│   ├── src/main/resources/
│   └── pom.xml
├── MedicalResponseApp/
│   ├── src/
│   ├── components/
│   ├── pages/
│   └── package.json
├── docs/
│   └── architecture.png
└── README.md
📦 Submission Packaging & Delivery
Steps Followed
Converted project repository into ZIP file

Included:

Source code

README.md

Architecture diagram

Uploaded ZIP to Google Drive

Generated public shareable link

Deliverables Submitted
Google Drive folder link (ZIP + README + diagram)

Project demo during review

⚖️ Ethics & Safety
No personal medical records stored

No real patient data used

System intended for academic and prototype purposes only

Does not replace professional medical services

🏆 Academic Compliance
Software-only solution

Real-world healthcare use case

No paid APIs or services

Clear documentation and architecture

Easy to test and demonstrate

📜 License

MIT License
