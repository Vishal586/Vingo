# Vingo

# 🍽️ Vingo – Restaurant Ordering & Management System

**Vingo** is a full-stack restaurant ordering and management system built using the **MERN (MongoDB, Express.js, React.js, Node.js)** stack.
It provides two separate dashboards for **owners** and **users**, enabling a seamless digital experience for both restaurant management and customers.
The platform allows restaurant owners to manage menu items, track orders, handle payments, and view analytics, while customers can browse food categories, place orders, and make secure payments.

---

## 🚀 Features

### 👨‍💼 For Restaurant Owners

* Secure **authentication** using JWT.
* Manage menu items – add, update, or delete food listings.
* View daily, weekly, and monthly order statistics.
* Integrated **Cloudinary** support for image uploads.
* Access to **Razorpay** integration for online transactions.
* Email notifications for order updates.

### 🍴 For Users

* Smooth **login/sign-up** experience with Firebase authentication.
* Browse menu items by category and price.
* Add items to cart, place orders, and make payments securely.
* Track order status in real time.
* Mobile-responsive and clean UI built with React + Vite.

---

## 🧰 Tech Stack

**Frontend:** React.js (Vite), Redux, React Router, Tailwind CSS, Firebase
**Backend:** Node.js, Express.js, JWT Authentication, Nodemailer, Cloudinary, Razorpay
**Database:** MongoDB (Atlas or Local)
**Deployment Options:** Vercel (frontend) and Render/Heroku (backend)

---

## ⚙️ Project Setup

### 1️⃣ Prerequisites

* Node.js v18+
* MongoDB (local or Atlas cloud)
* Cloudinary account (for image upload)
* Razorpay test keys (for payments)
* Firebase project (for authentication)

---

### 2️⃣ Backend Setup

1. Open a terminal:

   ```bash
   cd 8.vingo/backend
   npm install
   ```
2. Create a `.env` file and add:

   ```env
   PORT=8000
   MONGODB_URL=mongodb://localhost:27017/vingo
   JWT_SECRET=your_jwt_secret
   EMAIL=your_email@example.com
   PASS=your_email_app_password
   CLOUDINARY_CLOUD_NAME=your_cloud_name
   CLOUDINARY_API_KEY=your_api_key
   CLOUDINARY_API_SECRET=your_api_secret
   RAZORPAY_KEY_ID=your_key_id
   RAZORPAY_KEY_SECRET=your_key_secret
   ```
3. Start the backend server:

   ```bash
   npm run dev
   ```

   Server runs at **[http://localhost:8000](http://localhost:8000)**

---

### 3️⃣ Frontend Setup

1. In another terminal:

   ```bash
   cd 8.vingo/frontend
   npm install
   ```
2. Create a `.env` file:

   ```env
   VITE_FIREBASE_APIKEY=your_firebase_api_key
   VITE_GEOAPIKEY=your_geo_api_key
   VITE_RAZORPAY_KEY_ID=your_key_id
   ```
3. Start the development server:

   ```bash
   npm run dev
   ```

   Access the app at **[http://localhost:5173](http://localhost:5173)**

---

## 🧩 Folder Structure

```
8.vingo/
│
├── backend/            # Node.js + Express server
│   ├── routes/         # API routes
│   ├── models/         # MongoDB schemas
│   ├── controllers/    # Business logic
│   └── index.js        # App entry point
│
├── frontend/           # React + Vite app
│   ├── src/
│   │   ├── components/ # UI Components (Nav, Dashboards, etc.)
│   │   ├── pages/      # Screens and routing views
│   │   └── App.jsx     # Main app component
│
└── README.md
```

---

## 🧠 Key Fix Applied

The import path for the navigation component was corrected:

```diff
- import Nav from './NaV.JSX'
+ import Nav from './Nav'
```

This fix resolves the **Vite import-analysis error** during frontend build.

---

## 💡 Future Enhancements

* Add order delivery tracking via WebSockets.
* Implement admin analytics dashboard.
* Enable coupon and referral systems.
* Add push notifications for order updates.

---

## 🧾 License

This project is open-source under the **MIT License**. You are free to use, modify, and distribute it with attribution.
