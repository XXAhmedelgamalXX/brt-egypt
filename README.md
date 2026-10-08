# 🚌 BRT Tracker (Cairo Ring Road)

![Live Status](https://img.shields.io/badge/Status-Live-success)
![Version](https://img.shields.io/badge/Version-1.0-blue)
![Security](https://img.shields.io/badge/Security-Firestore_Rules-red)
![License](https://img.shields.io/badge/License-MIT-green)

A real-time, interactive crowdsourcing web application designed to map and track the new Bus Rapid Transit (BRT) stations along the Greater Cairo Ring Road. 

Built with a focus on **Data Integrity**, **System Security**, and **Frictionless UX**, the platform allows volunteers to contribute station coordinates seamlessly while providing administrators with a robust, real-time dashboard for verification and auditing.

---

## 🚀 Live Demo
**[Experience BRT Tracker Here](https://XXAhmedelgamalXX.github.io/brt-egypt/)**

---

## 🛡️ Security & Architecture (Highlight)

As a CS and Cybersecurity student, securing the system against unauthorized access and data manipulation was a primary objective:

1. **Strict Firestore Security Rules:** Implemented severe read/write access controls. The public can only *write* to the `pending_stations` collection but cannot read from it. Only authenticated admins can read, verify, or delete records.
2. **Device Fingerprinting (No-Auth Tracking):** Engineered a silent local device-ID generation system. This allows the system to accurately track top contributors and assign points to the `leaderboard` without forcing users through a tedious login/signup process, ensuring a high contribution rate.
3. **Hidden Admin Portal:** The Admin panel is deliberately isolated from the public UI. It is accessed via a logical "secret door" (a 5-click pattern on the footer developer name) to minimize public probing.
4. **Audit Logging:** The admin dashboard features a real-time Audit Log that tracks which admin approved or rejected a station, ensuring accountability within the management team.

---

## ✨ Key Features

### Public Facing
* **Interactive Mapping:** Utilizes `Leaflet.js` and OpenStreetMap to render a live, dynamic map of all verified BRT stations.
* **Smart Geolocation:** Automatically fetches the user's highly-accurate GPS coordinates upon approval.
* **Real-time Leaderboard:** Ranks top contributors based on verified data, encouraging community participation.
* **UI/UX Customization:** Features full Multilingual support (Arabic/English) and a seamless Dark/Light mode toggle.

### Admin Dashboard
* **Real-time Synchronization:** Uses Firebase `onSnapshot` listeners to update pending and verified tables instantly without page reloads.
* **Concurrency Control:** If an admin acts on a station, it instantly disappears from other admins' screens to prevent duplicate processing.
* **Data Export:** Integrated CSV generation for both pending and verified collections for external data analysis.

---

## 💻 Tech Stack
* **Frontend:** HTML5, CSS3, Vanilla JavaScript (ES6+).
* **Mapping Engine:** Leaflet.js.
* **Backend / BaaS:** Firebase (Firestore DB, Firebase Authentication).
* **Hosting:** GitHub Pages.

---

## 👨‍💻 Developer
**Ahmed Algamal**  
*Computer Science & Cybersecurity Student*  
* [GitHub](https://github.com/XXAhmedelgamalXX)
* [LinkedIn](https://www.linkedin.com/) *(Add your link here)*

---
*Feel free to explore the code, report issues, or suggest improvements!*
