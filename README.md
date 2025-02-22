# 📦 Deliveries System


A full-stack deliveries management system integrating **WhatsApp messages, Firebase, Azure AI, and real-time updates** for delivery tracking and assignment.

## 📌 Table of Contents
- [Overview](#-overview)
- [Architecture](#-architecture)
- [Technologies Used](#-technologies-used)
- [Usage](#-usage)
- [Repositories](#-repositories)
- [Installation](#-installation)

---

## 📌 Overview

Managing deliveries through WhatsApp groups can be chaotic, with multiple businesses sending orders in different formats. The Deliveries System automates this process, providing real-time tracking, organization, and AI-powered message processing—all while allowing managers to continue using WhatsApp.

🔹 What Problem Does It Solve?

The company receives delivery requests in 13 different WhatsApp groups, each with a unique format. Previously, managers had to manually track, organize, and assign deliveries. This system automates the process by extracting order details from messages and images, instantly assigning deliveries to workers, and keeping everything organized.

🔹 Features

✅ WhatsApp Integration – Automatically reads and processes orders from business groups.

✅ Real-Time Tracking – Instantly updates assigned deliveries and statuses in the app.

✅ AI-Powered Image Analysis – Extracts details like address, contact info, and order items from delivery photos.

✅ User-Friendly App – Designed for efficiency and safety, the app provides:

- One-tap navigation with Waze for quick routes.
- Instant communication with customers via a call button.
- Smart organization, allowing sorting and filtering by business, time, or status.
- Reduced phone use while driving, ensuring safer operations.

✅ Secure Authentication – Role-based access for managers and drivers.

---

# 📌 Technologies Used

### Backend
- **Node.js - Express** – REST API
- **Firebase Functions** – processes WhatsApp messages and triggers AI analysis.
- **Firebase Firestore** – Stores structured data like businesses details and WhatsApp messages.
- **Firebase Realtime Database** – Stores real-time delivery updates and user statuses.
- **Firebase Authentication** – Manages secure user logins.
- **Firebase Notifications** – Sends real-time alerts to users.
- **Socket.io** – Enables live updates between the server and the app.
- **Azure Computer Vision** – Extracts order details from delivery images.
- **Green API** – Connects to WhatsApp Webhooks for message retrieval.

### Frontend (Mobile App)
- **React Native + Expo** – Cross-platform mobile development
- **React Navigation** – Stack and tab navigation
- **Styled Components** – UI styling
- **React Hooks** – State management



---

## 📌 Architecture

![02F3DA37-7A08-4F2D-BB8C-E01B8A5EA51A](https://github.com/user-attachments/assets/4bcaa6f7-bea2-4ed2-80b9-0e4193a3aabd)

### 🔹 System Flow  

1. **Incoming WhatsApp Messages**  
   - Businesses send delivery pictures via **WhatsApp groups**.  
   - A **webhook (Green API)** captures and forwards messages to **Firebase Firestore**.  

2. **Processing and Data Extraction**  
   - A **Firebase Cloud Function** analyzes messages and images.  
   - **Azure Computer Vision** extracts relevant details like:  
     - Customer phone number  
     - Delivery address  
     - Business name (mapped from **chatId** in WhatsApp).  
     - Delivery time.  
   - The extracted data is structured and stored in **Firebase Realtime Database**.  

3. **Authentication & User Roles**  
   - **Firebase Authentication** manages user sign-in.  
   - Supports **admin (manager)** and **worker (delivery personnel)** roles.  
   - Each request to the backend includes a **JWT token** for secure access.  

4. **Real-Time Updates and Tracking**  
   - The **Node.js backend** listens for updates in Firebase.  
   - **Socket.io** pushes instant updates to connected devices.  

5. **Protected REST API (Express.js)**  
   - Backend provides **CRUD operations** for managing deliveries.  
   - Routes are **role-restricted**:  
     - 🛠 **Admin:** Can create, update, assign, and delete deliveries.  
     - 📦 **Worker:** Can only view and update assigned deliveries.  
   - API requests require a **valid authentication token**.  

6. **Mobile App (React Native) for Delivery Personnel**  
   - Displays assigned deliveries in real time.  
   - Provides **one-tap Waze navigation** and **quick call** options for safe and efficient driving.  
   - Allows status updates (e.g., "Delivered").  

This ensures a **secure, automated, and real-time delivery management system.  
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

