# 📦 Deliveries System


A full-stack deliveries management system integrating **WhatsApp messages, Firebase, Azure AI, and real-time updates** for delivery tracking and assignment.

## 📌 Table of Contents
- [Overview](#overview)
- [Architecture](#architecture)
- [Technologies Used](#technologies-used)
- [Usage](#usage)
- [Repositories](#repositories)
- [Installation](#installation)
  
---

## 📌 Overview
The Deliveries System helps shift manager manage deliveries by **automating WhatsApp order processing** and **tracking deliveries in real-time**.

### 🔹 Users:
1. **Admin (Manager):** Can view, assign, and track all deliveries.
2. **worker:** Receives assigned deliveries in real time and updates the status.

### 🔹 Features:
✅  **WhatsApp Integration:** Auto-processes messages from businesses.

✅  **Real-time Delivery Tracking:** Assign deliveries and get instant updates.

✅  **AI-Powered Image Analysis:** Extracts details from delivery images.

✅  **Sorting & Filtering:** Sort deliveries by time or business.

✅  **Navigation & Quick Actions** – One-tap Waze navigation and call options (hands-free driving safety).

✅  **Secure Authentication:** Role-based access (admin / worker).

---

## 📌 Architecture
The system is built with **React Native (Frontend), Node.js (Backend), Firebase, and Azure AI** for processing WhatsApp messages.

![image](https://github.com/user-attachments/assets/b0b1f573-2998-4ccc-a976-c2e0c63f0580)


### 🔹 How It Works:
1. **Incoming WhatsApp messages** → Firebase Firestore (via webhook & green api).
2. **Firebase Function processes messages**:
   - Analyzes images with **Azure Computer Vision**.
   - Extracts details (phone, address, business name, time).
   
3. **Deliveries stored in Firebase Realtime Database**.
4. **Node.js Server Listens for Changes**:
   - Uses **WebSockets (Socket.io)** for real-time updates.
5. **React Native App (Frontend) displays updates**.

---

## 📌 Technologies Used

### Backend
- **Node.js + Express** – REST API
- **Firebase Functions** – Background message processing
- **Firebase Firestore** – Stores incoming WhatsApp messages & businesses details
- **Firebase Realtime Database** – Stores deliveries according date & users info
- **Firebase Authentication**
- **Firebase Notifications**
- **Socket.io** – Real-time updates
- **Azure Computer Vision** – Extracts text from images
- **Green Api** - webhook endpoint

### Frontend (Mobile App)
- **React Native + Expo**
- **React Navigation** (Stacks, Tabs)
- **Styled Components** – UI styling
- **hooks**


---

## 📌 Usage

### 🔹 Admin Panel (Manager):
- View all incoming deliveries.
- Assign tasks to workers.
- Track delivery progress.
- Add new user to system.

### 🔹 Delivery Personnel App:
- See assigned deliveries in real time.
- Open Waze for directions && make phone call in a buttom press.
- Update status ("Delivered").

---

## 📂 Repositories
🔹 **Frontend (React Native App)** ➝ [Frontend Repo](https://github.com/RoiMeshulam/Deliveries_front)

🔹 **Backend (Node.js Server, Firebase Functions)** ➝ [Backend Repo](https://github.com/RoiMeshulam/Deliveries_backend)

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
   node server
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

