<div align="center">

# BunkVerse

### Smart Attendance & Bunk Management System for Students

**The goal isn't just to bunk; it's to plan your adventures without losing your attendance.**

[![Google Play](https://img.shields.io/badge/Google%20Play-Download%20BunkVerse-414141?style=for-the-badge&logo=google-play&logoColor=white)](https://play.google.com/store/apps/details?id=com.amoghvp.bunkverse)

</div>

---

## About

BunkVerse is a student-focused attendance management application designed to make attendance tracking, analysis, and planning easier.

Instead of simply displaying an attendance percentage, BunkVerse introduces the **Bunk Bank** — a system that helps students understand how many classes they can safely miss, carry unused bunks forward, or borrow from future months when necessary.

BunkVerse is designed around the idea of **planning attendance responsibly**, giving students a clearer picture of their attendance situation without relying on manual calculations.

---

# Features

## 🏦 Bunk Bank

The core system behind BunkVerse.

- **Available Bunks** — See how many classes can be safely missed.
- **Bunk Pass** — Carry unused bunks from completed months into the next month.
- **Bunk Loan** — Borrow bunks from future months when additional flexibility is needed.
- **Medical Leave** — Convert eligible past absences into medical leave.
- **Undo** — Reverse recent bunk loans or medical-leave changes.
- **Ledger Reset** — Reset a month's bunk ledger while automatically returning borrowed bunks to their original months.

The Bunk Bank is designed to turn complicated attendance calculations into an easier-to-understand planning system.

---

## 📅 Attendance Tracking

BunkVerse provides a calendar-based system for recording and managing daily attendance.

Students can record:

- **Full Day Present**
- **Absent**
- **Partial Attendance** — Select individual subjects attended on a particular day.

The attendance calendar uses visual indicators to make the current situation easy to understand:

- 🟢 **Green** — Safe
- 🟡 **Yellow** — Caution
- 🔴 **Red** — Danger

BunkVerse also accounts for days that should not affect attendance calculations, including:

- Sundays
- Holidays
- Examination days

### Quick Attendance Management

For faster data entry, users can long-press and select a date range to apply attendance changes across multiple days.

This is useful for:

- Holidays
- Examination periods
- Multiple-day attendance updates
- Clearing previously entered attendance

### Schedule Adjustments

Real-world schedules don't always follow the timetable.

BunkVerse supports:

- **Cancelled Classes** — Remove specific scheduled classes from a particular day.
- **Extra Classes** — Add classes that were not part of the normal timetable.

---

## 🗓️ Saturday & Weekend Support

Saturday schedules can vary significantly between colleges, so BunkVerse provides flexible weekend scheduling options.

Users can:

- **Copy a timetable** from any weekday to Saturday.
- Create a **custom half-day Saturday schedule**.
- Directly record attendance for **weekend classes**.

This allows BunkVerse to adapt to different college schedules instead of assuming every Saturday follows the same pattern.

---

## ⏰ Timetable & Subject Management

BunkVerse includes a flexible weekly timetable system designed to reduce manual schedule configuration.

- Class timings are automatically calculated based on the duration assigned to each subject.
- **Lunch breaks** can be configured independently for each day.
- The timetable automatically skips configured lunch periods.
- Subjects can use short codes such as `DBMS` or `MATH` for a cleaner interface while retaining their full names internally.
- Weekly schedules can be customized according to the student's actual college timetable.

---

## 📊 Attendance Reports & Analytics

BunkVerse provides detailed attendance reports to help students understand their attendance over different periods.

Reports can be generated for:

- **Entire Semester**
- **Individual Months**
- **Custom Date Ranges**

Users can also view attendance:

- Across **all subjects**
- For a **specific subject**

Attendance is presented using visual progress indicators and simple status categories:

- 🟢 **Green** — 75% or above
- 🟡 **Yellow** — 60–74%
- 🔴 **Red** — Below 60%

This makes it easier to identify attendance trends and understand which subjects may require attention.

---

## 💾 Privacy & Offline Storage

BunkVerse follows a **local-first approach** to attendance management.

There is:

- No account registration
- No cloud-based attendance tracking
- No requirement for cloud storage
- No need to send attendance data to external servers

Attendance records, timetable information, subjects, Bunk Bank data, and application settings are stored locally on the user's device.

The core attendance-management functionality is designed to work without requiring a constant internet connection.

Internet connectivity is primarily required for services such as advertisements.

---

## 📤 Backup & Restore

BunkVerse includes a CSV-based backup system that allows users to export their application data for personal backup or transfer purposes.

The exported backup file is:

`BunkVerse_Backup.csv`

The backup can contain information such as:

- Subjects
- Attendance records
- Timetable data
- Bunk Bank information
- Application settings

This provides users with a way to maintain a personal copy of their data without relying on cloud storage.

---

## 📖 Built-in Tutorial

BunkVerse includes a built-in tutorial to help users understand the application's features and workflows.

The tutorial is stored locally as a Markdown file and is converted into HTML before being displayed inside a styled WebView.

This allows the tutorial to remain integrated within the application without requiring users to open an external browser.

---

## 🧹 Complete Data Reset

BunkVerse provides a complete reset option for users who want to start over.

The reset process clears the application's locally stored database and preferences, returning BunkVerse to a fresh-install state.

---

# The Problem

College attendance is often reduced to a single percentage.

But knowing that you have **78% attendance** doesn't necessarily answer the questions students actually care about:

> *How many classes can I miss?*

> *Can I afford to skip tomorrow's class?*

> *How much attendance do I need to recover?*

> *What happens if I have already used my available bunks?*

> *Can I carry unused attendance flexibility into the next month?*

Students often rely on manual calculations, spreadsheets, or rough estimates to answer these questions.

BunkVerse was designed to make this process simpler and more understandable.

---

# The Idea

BunkVerse combines:

**Attendance Tracking + Timetable Management + Attendance Analytics + Bunk Planning**

into a single application.

The **Bunk Bank** system is the core concept behind the application. It transforms attendance calculations into a more understandable planning system by representing attendance flexibility as available bunks.

Students can see their current attendance situation, understand how much flexibility they have, and make more informed decisions about their attendance.

The objective is **not to encourage irresponsible attendance**.

Instead, BunkVerse is designed to help students understand their attendance and plan their schedules responsibly.

> **"The goal isn't just to bunk; it's to plan your adventures without losing your attendance."**

---

# Technology & Architecture

BunkVerse is built as a **local-first Android application** using Java.

The application uses a repository-based architecture to separate data handling from the user interface and application logic.

## Technology Stack

| Component | Technology |
|---|---|
| Language | Java |
| Platform | Android |
| Local Database | Room / SQLite |
| UI Components | Material Components |
| Serialization | Gson |
| Animations | Lottie |
| Tutorial Rendering | WebView |
| Advertising | Google AdMob |
| Minimum SDK | API 24 (Android 7.0) |
| Target SDK | API 36 |

## Local Data Architecture

BunkVerse stores application data locally on the user's device.

The local database is responsible for managing information such as:

- Attendance records
- Subjects
- Timetable configuration
- Bunk Bank data
- Attendance-related settings

This local-first approach allows the core attendance-management functionality to operate without requiring a constant internet connection.

---

# User Interface

BunkVerse uses a futuristic **dark HUD-inspired interface** designed around information clarity and visual feedback.

The visual system includes:

- Dark backgrounds
- Bright cyan accents
- Glass-style UI components
- HUD-inspired indicators
- Animated interface elements
- Visual attendance status indicators

### Visual Identity

| Element | Value |
|---|---|
| Primary Background | `#060E1C` |
| Accent | `#00B4FF` |
| Design Language | Futuristic / HUD |
| Theme | Dark |

---

# Screenshots

> Screenshots will be added here.

---

# Project Information

| Property | Details |
|---|---|
| **Project** | BunkVerse |
| **Developer** | Amogh V P |
| **Creator Name** | AmoghVP |
| **Platform** | Android |
| **Language** | Java |
| **Package** | `com.amoghvp.bunkverse` |
| **Current Version** | 1.6 |
| **Build** | 6 |
| **Minimum SDK** | API 24 |
| **Target SDK** | API 36 |
| **Database** | Room / SQLite |
| **License** | Proprietary / Private |

---

# Source Code

The BunkVerse application source code is **proprietary and is not publicly available**.

This repository is a **project showcase and documentation repository**, intended to provide information about BunkVerse and its development.

It may contain:

- Project documentation
- Feature descriptions
- Architecture information
- Screenshots
- Visual assets
- Development information
- Release information

It does **not** contain:

- Application source code
- Android Studio project files
- Signing keys
- Private credentials
- API secrets
- Production databases
- Other confidential development resources

The BunkVerse source code remains privately maintained by the developer.

---

# Download BunkVerse

BunkVerse is available on Google Play.

[![Get it on Google Play](https://img.shields.io/badge/Google%20Play-Download%20BunkVerse-414141?style=for-the-badge&logo=google-play&logoColor=white)](https://play.google.com/store/apps/details?id=com.amoghvp.bunkverse)

---

# Developer

## Amogh V P

**AmoghVP**

BunkVerse is an independently developed student-focused application created to solve a practical problem with attendance management and planning.

The project covers the complete development cycle from:

**Concept → UI/UX → Development → Database Architecture → Testing → Deployment → Google Play Publishing**

---

# Project Status

**Published on Google Play**

BunkVerse is an actively maintained project and may receive future updates, improvements, and additional platform support.

---

# Philosophy

BunkVerse isn't designed to encourage students to blindly skip classes.

It is designed to help students **understand their attendance, calculate their available flexibility, and make informed decisions**.

> **Track smarter. Plan better. Bunk responsibly.**

---

<div align="center">

## BunkVerse

**Smart attendance. Smarter planning.**

</div>
