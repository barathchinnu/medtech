


# 🚑 Smart Emergency Medical Response System

A **software-based emergency healthcare platform** designed to reduce response time during medical emergencies by connecting **patients, ambulance drivers, and hospitals** through a real-time, Uber-style workflow.

---
## Problem Statement
In emergency medical situations, delays often occur due to lack of coordination between patients, ambulance services, and hospitals. Manual communication and absence of real-time systems lead to increased response time, which can result in loss of life.


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

if you need to see our project along with database we have not hosted to main so if you use it you can gone through the under given steps
---We Uploaded Our Project in Google Drive as Docker Read the following instructions to Run the project
This guide explains step by step how to extract the project from Google Drive, install Docker, and run the backend using a Dockerfile.

📥 Step 1: Download Project from Google Drive

Open the shared Google Drive link

Right-click the project folder or ZIP file

Click Download

The file will be downloaded as a .zip file

Example:

medical-response-backend.zip

📂 Step 2: Extract the ZIP File

Go to your Downloads folder

Right-click the ZIP file

Click Extract All

Choose a location and click Extract

After extraction, you should see a folder like:

medical-response-backend/
 ├── Dockerfile
 ├── pom.xml
 ├── src/
 ├── target/


⚠️ Make sure the Dockerfile is present.

🐳 Step 3: Install Docker Desktop (Mandatory)

Docker is required to run this project.

🔹 Download Docker Desktop

👉 https://www.docker.com/products/docker-desktop/

Click Download for Windows

🔹 Install Docker Desktop

During installation:

✅ Enable WSL 2

✅ Add Docker to PATH

✅ Use default settings

After installation, restart your system 🔄

✅ Step 4: Verify Docker Installation

Open PowerShell and run:

docker --version


Expected output:

Docker version xx.x.x


If this works, Docker is installed correctly.

📁 Step 5: Navigate to Project Folder

Open PowerShell and go to the extracted folder:

cd path\to\medical-response-backend


Example:

cd C:\Users\YourName\Downloads\medical-response-backend


Check files:

dir


You must see:

Dockerfile

🏗 Step 6: Build the Docker Image

Run the following command:

docker build -t medtech-backend .


⏳ This may take a few minutes on the first run.

If successful, the build will complete without errors.

▶ Step 7: Run the Docker Container

Run the backend application:

docker run -p 8080:8080 medtech-backend


If port 8080 is already in use, try:

docker run -p 9090:8080 medtech-backend

🌐 Step 8: Access the Application

Open a web browser and go to:

http://localhost:8080


(or http://localhost:9090 if you used port 9090)

🧪 Helpful Docker Commands
Check running containers
docker ps

Stop the container
Ctrl + C


or

docker stop <container_id>

View logs
docker logs medtech-backend
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


