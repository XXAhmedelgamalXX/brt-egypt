# 🚌 BRT Tracker (Cairo Ring Road) | مسار الأتوبيس الترددي

![Live Status](https://img.shields.io/badge/Status-Live-success)
![Version](https://img.shields.io/badge/Version-1.0-blue)
![Security](https://img.shields.io/badge/Security-Firestore_Rules-red)
![License](https://img.shields.io/badge/License-MIT-green)

🌍 **[🇪🇬 للنسخة العربية، انزل للأسفل أو اضغط هنا](#-النسخة-العربية-arabic-version)**

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

<br><br>
---
---

## 🇪🇬 النسخة العربية (Arabic Version)

تطبيق ويب تفاعلي يعتمد على التعهيد الجماعي (Crowdsourcing) لرسم وتتبع محطات الأتوبيس الترددي (BRT) على الطريق الدائري بالقاهرة الكبرى.

تم بناء النظام مع التركيز على **سلامة البيانات**، **أمن النظام**، وتوفير **تجربة مستخدم سلسة**، مما يتيح للمتطوعين إضافة الإحداثيات الجغرافية للمحطات بسهولة، مع توفير لوحة تحكم لحظية (Real-time Dashboard) للإدارة للمراجعة والتدقيق.

---

### 🚀 المعاينة الحية
**[جرب النظام الفعلي من هنا](https://XXAhmedelgamalXX.github.io/brt-egypt/)**

---

### 🛡️ الهندسة الأمنية (Security Architecture)

بصفتي طالب علوم حاسب وأمن سيبراني، كان تأمين النظام ضد التلاعب أو الوصول غير المصرح به هدفاً أساسياً:

1. **قواعد حماية Firestore الصارمة:** تطبيق قيود حازمة على قراءة وكتابة البيانات. يمكن للجمهور *إضافة* المحطات فقط (Write) إلى مجموعة `pending_stations` ولا يمكنهم قراءتها. في حين يقتصر حق القراءة، الاعتماد، والحذف على حسابات الإدارة المصرح لها فقط.
2. **بصمة الجهاز (Device Fingerprinting):** هندسة نظام لتوليد هويات محلية صامتة (Device IDs) لتتبع المساهمين وحساب النقاط في "لوحة الشرف" دون إجبارهم على إنشاء حسابات أو تسجيل الدخول، مما يضمن زيادة معدل المشاركة.
3. **بوابة الإدارة المخفية:** تم عزل لوحة تحكم الإدارة تماماً عن واجهة الجمهور. يمكن الوصول إليها فقط عبر "باب سري" برمجي (الضغط 5 مرات على اسم المطور في الفوتر) لتقليل محاولات الاختراق أو العبث (Probing).
4. **سجل النشاطات (Audit Logging):** تحتوي لوحة الإدارة المشتركة على سجل نشاطات لحظي يتتبع كل مشرف (Admin) والإجراء الذي اتخذه (قبول/رفض المحطة) لضمان المساءلة والمراقبة داخل فريق الإدارة.

---

### ✨ أهم المميزات

**واجهة الجمهور:**
* **الخريطة التفاعلية:** استخدام محرك `Leaflet.js` مع OpenStreetMap لعرض مسار المحطات المعتمدة بشكل تفاعلي.
* **الموقع الجغرافي الذكي:** التقاط إحداثيات (GPS) الدقيقة للمستخدم بمجرد إعطاء الصلاحية للمتصفح.
* **لوحة الشرف اللحظية:** ترتيب المتطوعين بناءً على محطاتهم المعتمدة لتشجيع المنافسة.
* **تخصيص الواجهة:** دعم كامل للغتين (العربية/الإنجليزية) ووضع الإضاءة (Dark/Light Mode).

**لوحة تحكم الإدارة:**
* **المزامنة اللحظية (Real-time Sync):** الاعتماد على تقنية `onSnapshot` من Firebase لتحديث جداول المحطات (المنتظرة والمعتمدة) فوراً وبدون إعادة تحميل الصفحة.
* **التحكم في التزامن (Concurrency Control):** عند التعامل مع محطة من قِبل أحد المشرفين، تختفي فوراً من شاشات المشرفين الآخرين لمنع تكرار الاعتماد.
* **تصدير البيانات:** دعم استخراج البيانات بصيغة (CSV Export) لتحليلها خارجياً.

---

### 💻 التقنيات المستخدمة
* **الواجهة الأمامية (Frontend):** HTML5, CSS3, Vanilla JavaScript (ES6+).
* **محرك الخرائط:** Leaflet.js.
* **الواجهة الخلفية وقواعد البيانات (Backend/BaaS):** Firebase (Firestore DB, Firebase Authentication).
* **الاستضافة (Hosting):** GitHub Pages.

---

## 👨‍💻 Developer / المطور
**Ahmed Algamal | أحمد وليد أحمد الجمل**  
*Computer Science & Cybersecurity Student | طالب علوم حاسب وأمن سيبراني*  
* [GitHub](https://github.com/XXAhmedelgamalXX)
* [LinkedIn](https://www.linkedin.com/in/ahmed-algamal-4995993b4/)

---
*Feel free to explore the code, report issues, or suggest improvements!*  
*لا تتردد في استكشاف الكود، الإبلاغ عن أي مشاكل، أو اقتراح تحسينات!*
