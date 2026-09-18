<div align="center">

<img src="app/src/main/res/mipmap-xxxhdpi/ic_launcher_round.png" alt="BunkVerse Logo" width="180">

# BunkVerse

### The Ultimate Futuristic Attendance & Bunk Bank Manager

**"The goal isn't just to bunk; it's to plan your adventures without losing your attendance."**

[![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://developer.android.com/)
[![Language](https://img.shields.io/badge/Language-Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)](https://www.java.com/)
[![Target SDK](https://img.shields.io/badge/Target_SDK-36-00B4FF?style=for-the-badge&logo=android)](https://developer.android.com/about/versions/15)

</div>

---

## 🌌 About BunkVerse

**BunkVerse** is a high-tech, student-centric Android application that treats your college attendance like a financial ledger. Designed with a futuristic **HUD-style Dark Theme** (`#060E1C` with Cyan accents), it moves beyond simple percentage tracking to provide a comprehensive **Bunk Bank** system.

Whether you're planning a trip, dealing with medical issues, or just need a break, BunkVerse calculates exactly how much "attendance currency" you have to spend while keeping you above your college's required threshold.

---

## 🚀 Key Subsystems

### 💳 The "Bunk Bank" Ledger
Treat your skips like a bank account. 
*   **Available Bunks:** Real-time calculation of safe skips remaining.
*   **Bunk Pass:** Carry forward surplus attendance to the next month.
*   **Bunk Loan:** Borrow skips from future months if you have a projected surplus.
*   **Medical Leave:** Neutralize absences so they don't impact your official percentage.
*   **Safety Undo:** A dedicated ledger system to reverse recent loans or medical entries.

### 🤖 ZUMI — The Local Assistant
BunkVerse features **ZUMI**, a specialized local engine (`AssistantEngine.java`) that allows you to interact with your data using natural language.
*   *"Can I bunk DBMS today?"*
*   *"What is my overall attendance?"*
*   *"Show me my timetable for tomorrow."*
*   **Privacy-First:** All processing happens locally; your queries never leave your device.

### 📅 Smart HUD Calendar & Logging
*   **Range Logging:** Long-press to bulk-log entire weeks of holidays or exam durations.
*   **Exclusion Logic:** Automatically excludes Sundays, Holidays, and Exams for fair statistical reporting.
*   **Saturday Special:** Flexible logic to borrow any weekday's timetable or set a custom manual half-day schedule.
*   **Daily Overrides:** Handle "Classes Cancelled" or "Extra Classes" on the fly without breaking your core timetable.

### 🕒 HUD Timetable Management
*   **Auto-Duration:** Enter subject duration (mins), and the app auto-calculates slot end-times.
*   **Lunch Logic:** Per-day custom lunch break configurations that are automatically skipped during logging.
*   **Full Viewer:** A dedicated horizontal scrolling day selector for a crisp overview of your week.

---

## 📊 Analytics & Reporting

BunkVerse provides high-density visual feedback using custom circular progress bars and color-coded status markers:

- 🟢 **SAFE (≥ 75%)** — You have a healthy bunk balance.
- 🟡 **CAUTION (60–74%)** — Approach the bunk limit with care.
- 🔴 **DANGER (< 60%)** — Immediate attendance recovery required.

Reports are available for the full **Semester**, **Monthly breakdowns**, or **Custom Date Ranges**.

---

## 🛠 Technology Stack

| Component | Technology |
|---|---|
| **Language** | Java |
| **Architecture** | Local-First / Repository Pattern |
| **Database** | **Room Persistence Library** (SQLite) |
| **UI Framework** | Material 3 (M3) + Custom HUD XML |
| **Animations** | Lottie + Layout Transition API |
| **Utilities** | Gson, WebView (Markdown Parser) |
| **Minimum SDK** | API 24 (Android 7.0) |
| **Target SDK** | API 36 (Android 15 Preview) |

---

## 🛡️ Privacy & Data Portability

*   **100% Offline:** No account creation, no cloud syncing, and zero tracking.
*   **CSV Backup Engine:** Export your entire life — subjects, logs, loans, and settings — into a single `BunkVerse_Backup.csv`.
*   **Markdown Tutorial:** A built-in documentation engine that parses `tutorial.md` into a styled HTML viewer.
*   **Self-Destruct:** A one-tap **Full Reset** mechanism to wipe all data instantly.

---

## 👨‍💻 Developer Information

**BunkVerse** is a solo project developed by **Amogh V P (AmoghVP)**. 

> *"I built BunkVerse because keeping track of attendance across complex schedules, holidays, and medical leaves is a mathematical nightmare. This app gives you the data; what you do with it is your call."*

---

## 📄 License

**Proprietary / Private Development**  
All rights reserved by the developer. This repository serves as a showcase of the application's architecture and feature set.

---

<div align="center">

**Track smarter. Plan better. Bunk responsibly.**  
Built with 💻 and ☕ by AmoghVP.

</div>
