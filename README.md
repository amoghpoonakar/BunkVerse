<div align="center">

<img src="assets/bunkverse-logo.png" alt="BunkVerse Logo" width="180">

# BunkVerse

### Smart Attendance & Bunk Management System for Students

**The goal isn't just to bunk; it's to plan your adventures without losing your attendance.**

[![Google Play](https://img.shields.io/badge/Google%20Play-Download%20BunkVerse-414141?style=for-the-badge&logo=google-play&logoColor=white)](https://play.google.com/store/apps/details?id=com.amoghvp.bunkverse)

</div>

---

## About

BunkVerse is a student-focused attendance management application designed to make attendance tracking, analysis, planning, and timetable management easier.

Instead of simply displaying an attendance percentage, BunkVerse introduces the **Bunk Bank** — a system that helps students understand how many classes they can safely miss, carry unused bunks forward, or borrow from future months when necessary.

BunkVerse also includes **ZUMI**, a built-in student assistant that lets users interact with their timetable, attendance, and Bunk Bank information through natural-language questions.

BunkVerse is designed around the idea of **planning attendance responsibly**, giving students a clearer picture of their attendance situation without relying on manual calculations.

---

## Features

### Bunk Bank

The core system behind BunkVerse.

- Available Bunks
- Bunk Pass
- Bunk Loan
- Medical Leave
- Undo
- Ledger Reset

[View the complete Bunk Bank documentation →](docs/BUNK_BANK.md)

### ZUMI — Student Assistant

ZUMI is BunkVerse's built-in local assistant for interacting with timetable, attendance, and Bunk Bank information.

Users can ask questions such as:

- "What classes do I have today?"
- "What's my timetable tomorrow?"
- "What's my attendance in OS?"
- "How many bunks do I have left?"
- "Can I bunk DBMS today?"
- "What classes can I bunk this month?"

ZUMI supports natural variations of common questions and lightweight conversational follow-ups. It can also use Android speech recognition for voice input.

For bunk-related questions, ZUMI uses the application's Bunk Bank data, including available, used, and remaining bunks, rather than maintaining a separate bunk balance.

### Attendance Tracking

Calendar-based attendance management supporting:

- Full Day Present
- Absent
- Partial Attendance
- Date-range attendance management
- Holidays
- Examination days
- Cancelled classes
- Extra classes

### Timetable & Subject Management

- Flexible weekly timetable
- Automatic class timing calculation
- Per-day lunch breaks
- Custom subject short codes
- Weekday-to-Saturday timetable copying
- Custom Saturday schedules
- Weekend class support

### Reports & Analytics

Generate attendance reports for:

- Entire semester
- Individual months
- Custom date ranges
- All subjects
- Individual subjects

Attendance status is represented as:

- 🟢 **Safe** — 75% or above
- 🟡 **Caution** — 60–74%
- 🔴 **Danger** — Below 60%

### Privacy & Offline Storage

BunkVerse follows a **local-first approach**.

Attendance, timetable, subject, Bunk Bank, and application settings are stored locally on the device.

There is no account registration or cloud-based attendance tracking.

ZUMI's core timetable, attendance, and Bunk Bank functionality works with the information available inside the application.

### Backup

Application data can be exported as:

`BunkVerse_Backup.csv`

The backup can contain subjects, attendance records, timetable data, Bunk Bank information, and application settings.

---

## Screenshots

### Homepage

<img src="screenshots/1_Homepage.png" alt="BunkVerse Dashboard" width="300">

### Attendance Calendar

<img src="screenshots/3_AttendaceLog.png" alt="BunkVerse Attendance Calendar" width="300">

### Timetable

<img src="screenshots/5_Timetable.png" alt="BunkVerse Timetable" width="300">

### Reports & Analytics

<img src="screenshots/4_Summary.png" alt="BunkVerse Reports" width="300">

### Bunk Bank

<img src="screenshots/8_BunkBank_OG.png" alt="BunkVerse Bunk Bank" width="300">

---

## Technology Stack

| Component | Technology |
|---|---|
| Language | Java |
| Platform | Android |
| Local Database | Room / SQLite |
| UI | Material Components |
| Serialization | Gson |
| Animations | Lottie |
| Tutorial | WebView |
| Advertising | Google AdMob |
| Minimum SDK | API 24 |
| Target SDK | API 36 |

[View the architecture documentation →](docs/ARCHITECTURE.md)

---

## Project Information

| Property | Details |
|---|---|
| Project | BunkVerse |
| Developer | Amogh V P |
| Creator Name | AmoghVP |
| Current Version | 1.6 |
| Build | 6 |
| Package | `com.amoghvp.bunkverse` |
| Minimum SDK | API 24 |
| Target SDK | API 36 |
| Platform | Android |
| Language | Java |
| License | Proprietary / Private |

---

## Source Code

The BunkVerse application source code is **proprietary and is not publicly available**.

This repository is a **project showcase and documentation repository**.

It may contain:

- Feature documentation
- Architecture information
- Screenshots
- Visual assets
- Development information
- Release information

It does not contain:

- Application source code
- Android Studio project files
- Signing keys
- Private credentials
- API secrets
- Production databases
- Other confidential development resources

The BunkVerse source code remains privately maintained by the developer.

---

## Project Status

**Published on Google Play**

BunkVerse is an actively maintained project and may receive future updates, improvements, and additional platform support.

---

## Room for Improvement

BunkVerse is an actively evolving project. Future development can expand existing systems and introduce additional capabilities.

### ZUMI

ZUMI currently focuses on timetable, attendance, and Bunk Bank questions. Future improvements could make ZUMI a deeper conversational interface for BunkVerse.

Potential improvements include:

- More natural conversational context
- More complex multi-step questions
- Better understanding of follow-up questions
- Deeper timetable and attendance analysis
- More detailed Bunk Bank explanations
- More flexible date and time interpretation
- Expanded voice interaction
- More personalized student workflows
- Additional app actions through conversational commands
- Broader access to supported BunkVerse features

The long-term goal is for ZUMI to become a more deeply integrated way of interacting with BunkVerse while continuing to rely on the application's own data.

### Bunk Management

The Bunk Bank system can continue to evolve with additional planning and analysis capabilities.

Potential improvements include:

- More detailed monthly planning
- Additional bunk-management insights
- Expanded carry-forward options
- Improved bunk usage visualization
- More detailed historical analysis

### Attendance & Analytics

Future versions can expand attendance reporting and analytics with additional ways of understanding attendance trends and planning future attendance.

### User Experience

The application's interface and workflows can continue to be refined based on student feedback and real-world usage.

Potential improvements include:

- Faster attendance logging
- More streamlined timetable management
- Improved report visualization
- Additional customization options
- Better onboarding and tutorials

---

## Philosophy

BunkVerse isn't designed to encourage students to blindly skip classes.

It is designed to help students **understand their attendance, calculate their available flexibility, and make informed decisions**.

ZUMI follows the same philosophy by helping students access and understand their existing attendance, timetable, and Bunk Bank information more naturally.

> **Track smarter. Plan better. Bunk responsibly.**

---

## Developer

### Amogh V P

**AmoghVP**

BunkVerse is an independently developed student-focused application created to solve a practical problem with attendance management and planning.

The project covers the complete development cycle:

**Concept → UI/UX → Development → Database Architecture → Testing → Deployment → Google Play Publishing**

---

<div align="center">

## BunkVerse

**Smart attendance. Smarter planning.**

</div>
