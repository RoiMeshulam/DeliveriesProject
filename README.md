📦 Deliveries System
A full-stack deliveries management system integrating WhatsApp messages, Firebase, Azure AI, and real-time updates for delivery tracking and assignment.

📌 Table of Contents
Overview
Architecture
Repositories
Installation
Usage
Technologies Used
Contributing
🚀 Overview
The Deliveries System helps businesses manage deliveries by automating WhatsApp order processing and tracking deliveries in real-time.

👥 Users:
Admin (Manager): Can view, assign, and track all deliveries.
Delivery Personnel: Receives assigned deliveries in real time and updates the status.
🔹 Features:
✔️ WhatsApp Integration: Auto-processes messages from businesses.
✔️ Real-time Delivery Tracking: Assign deliveries and get instant updates.
✔️ AI-Powered Image Analysis: Extracts details from delivery images.
✔️ Sorting & Filtering: Sort deliveries by time or business.
✔️ Navigation Integration: Open Waze directly for the delivery address.
✔️ Secure Authentication: Role-based access (Admin / Delivery).

🛠️ Architecture
The system is built with React Native (Frontend), Node.js (Backend), Firebase, and Azure AI for processing WhatsApp messages.

📌 How It Works:
Incoming WhatsApp messages → Firebase Firestore (via webhook).
Firebase Function processes messages:
Extracts details (phone, address, business name).
Analyzes images with Azure Computer Vision.
Deliveries stored in Firebase Realtime Database.
Node.js Server Listens for Changes:
Uses WebSockets (Socket.io) for real-time updates.
React Native App (Frontend) displays updates.
📂 Repositories
🔹 Frontend (React Native App) ➝ GitHub Repo
🔹 Backend (Node.js Server, Firebase Functions) ➝ GitHub Repo

⚙️ Installation
🔹 Backend Setup
Clone the backend repo:
sh
Copy
Edit
git clone <backend-repo-url>
cd backend
npm install
Set up .env file (Environment Variables).
Start the backend server:
sh
Copy
Edit
npm start
🔹 Frontend Setup
Clone the frontend repo:
sh
Copy
Edit
git clone <frontend-repo-url>
cd frontend
npm install
Install dependencies:
sh
Copy
Edit
npm install expo-cli --global
Run the React Native app:
sh
Copy
Edit
npm expo start
Install on Android/iOS devices using Expo Go.
📌 Usage
🔹 Admin Panel (Manager):
View all incoming deliveries.
Assign deliveries to drivers.
Track delivery progress.
Call delivery personnel (hands-free).
🔹 Delivery Personnel App:
See assigned deliveries in real time.
Open Waze for directions.
Update status (e.g., "Picked Up", "Delivered").
🚀 Technologies Used
Backend
Node.js + Express – REST API
Firebase Functions – Background message processing
Firebase Firestore – Stores incoming WhatsApp messages
Firebase Realtime Database – Stores active deliveries
Socket.io – Real-time updates
Azure Computer Vision – Extracts text from images
Frontend (Mobile App)
React Native + Expo
React Navigation (Stacks, Tabs)
Styled Components – UI styling
Firebase Authentication
🤝 Contributing
If you’d like to contribute:

Fork the repository.
Create a new branch (feature/new-feature).
Submit a Pull Request.
