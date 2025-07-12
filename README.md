
# 🎓 Student-Teacher Booking Appointment App

A **Firebase-powered** web application that allows students to book appointments and teachers (admins) to approve or manage them through an intuitive admin dashboard.

---

## 🚀 Features

* 🔐 **Student Authentication** using Firebase Auth (Email/Password)
* 📅 **Appointment Booking** by students with date & time selection
* 🧑‍🏫 **Admin Dashboard** for teachers to approve or delete appointments
* ☁️ **Real-time Data Storage** with Firebase Firestore
* ✅ Responsive, simple, and easy to use

---

## 🛠️ Technologies Used

* **HTML5**, **CSS3**, **JavaScript**
* **Firebase Authentication**
* **Firebase Firestore (Cloud Database)**
* **Firebase Modular SDK (v9)**

---

## 📁 Project Structure

```
├── index.html           # Main UI with login & appointment form
├── style.css            # Custom styles
├── main.js              # App logic (auth, Firestore, admin checks)
├── firebase-config.js   # Firebase configuration
└── README.md            # Project overview and setup guide
```

---

## 🔧 Getting Started

1. **Clone or download** this repository.
2. Replace Firebase config values in `firebase-config.js` with your own.
3. In the Firebase Console:

   * Enable **Email/Password Authentication** under Authentication settings.
   * Create a **Cloud Firestore database**.
4. Use the following **Firestore security rules** for development:

```js
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.time < timestamp.date(2025, 8, 8);
    }
  }
}
```

---

## 👩‍🏫 Admin Access

Admins (teachers) are recognized by email:

```js
const adminEmails = ['admin@example.com']; // Replace with actual admin emails
```

Admins can:

* View all appointment requests
* Approve or delete appointments

---

## 📌 Future Improvements

* 🔄 Password reset functionality
* 📊 Pagination and filtering in the admin dashboard
* 🚀 Deploy via **Firebase Hosting**
* 📧 Email notifications with **Firebase Functions**

---

## 📜 License

**MIT License** — Free to use, modify, and distribute.

