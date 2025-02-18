# 📦 Deliveries System

A full-stack deliveries management system integrating **WhatsApp messages, Firebase, Azure AI, and real-time updates** for delivery tracking and assignment.

## 📌 Table of Contents
- [Overview](#overview)
- [Architecture](#architecture)
- [Repositories](#repositories)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)

---

## 🚀 Overview
The Deliveries System helps businesses manage deliveries by **automating WhatsApp order processing** and **tracking deliveries in real-time**.

### 👥 Users:
1. **Admin (Manager):** Can view, assign, and track all deliveries.
2. **Delivery Personnel:** Receives assigned deliveries in real time and updates the status.

### 🔹 Features:
✔️ **WhatsApp Integration:** Auto-processes messages from businesses.
✔️ **Real-time Delivery Tracking:** Assign deliveries and get instant updates.
✔️ **AI-Powered Image Analysis:** Extracts details from delivery images.
✔️ **Sorting & Filtering:** Sort deliveries by time or business.
✔️ **Navigation Integration:** Open Waze directly for the delivery address.
✔️ **Secure Authentication:** Role-based access (Admin / Delivery).

---

## 🛠️ Architecture
The system is built with **React Native (Frontend), Node.js (Backend), Firebase, and Azure AI** for processing WhatsApp messages.

### 📌 How It Works:
1. **Incoming WhatsApp messages** → Firebase Firestore (via webhook).
2. **Firebase Function processes messages**:
   - Extracts details (phone, address, business name).
   - Analyzes images with **Azure Computer Vision**.
3. **Deliveries stored in Firebase Realtime Database**.
4. **Node.js Server Listens for Changes**:
   - Uses **WebSockets (Socket.io)** for real-time updates.
5. **React Native App (Frontend) displays updates**.

---

## 📂 Repositories
🔹 **Frontend (React Native App)** ➝ [GitHub Repo](#)
🔹 **Backend (Node.js Server, Firebase Functions)** ➝ [GitHub Repo](#)

---

## ⚙️ Installation

### 🔹 Backend Setup
1. Clone the backend repo:
   ```sh
   git clone <backend-repo-url>
   cd backend
   npm install
   ```  
2. Set up **.env** file (Environment Variables).
3. Start the backend server:
   ```sh
   npm start
   ```  

### 🔹 Frontend Setup
1. Clone the frontend repo:
   ```sh
   git clone <frontend-repo-url>
   cd frontend
   npm install
   ```  
2. Install dependencies:
   ```sh
   npm install expo-cli --global
   ```  
3. Run the React Native app:
   ```sh
   npm expo start
   ```  
4. Install on **Android/iOS devices** using **Expo Go**.

---

## 📌 Usage

### 🔹 Admin Panel (Manager):
- View all incoming deliveries.
- Assign deliveries to drivers.
- Track delivery progress.
- Call delivery personnel (hands-free).

### 🔹 Delivery Personnel App:
- See assigned deliveries in real time.
- Open Waze for directions.
- Update status (e.g., "Picked Up", "Delivered").

---

## 🚀 Technologies Used

### Backend
- **Node.js + Express** – REST API
- **Firebase Functions** – Background message processing
- **Firebase Firestore** – Stores incoming WhatsApp messages
- **Firebase Realtime Database** – Stores active deliveries
- **Socket.io** – Real-time updates
- **Azure Computer Vision** – Extracts text from images

### Frontend (Mobile App)
- **React Native + Expo**
- **React Navigation** (Stacks, Tabs)
- **Styled Components** – UI styling
- **Firebase Authentication**

---

## 🤝 Contributing
If you’d like to contribute:
1. Fork the repository.
2. Create a new branch (`feature/new-feature`).
3. Submit a Pull Request.

---
