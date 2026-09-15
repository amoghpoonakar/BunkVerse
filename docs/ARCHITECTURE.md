# BunkVerse Architecture

BunkVerse is designed as a local-first Android application built using Java.

The architecture focuses on keeping attendance and timetable data locally available while separating data management from application logic and the user interface.

---

## Platform

BunkVerse is currently developed for Android.

| Property | Value |
|---|---|
| Language | Java |
| Minimum SDK | API 24 |
| Target SDK | API 36 |
| Package | `com.amoghvp.bunkverse` |

---

## Architecture Approach

BunkVerse follows a repository-based architecture.

The repository layer is responsible for separating data access and persistence from the rest of the application.

This approach helps keep:

- Data operations
- Application logic
- User interface

separated from each other.

---

## Local Database

BunkVerse uses Room / SQLite for local data storage.

The local database manages application information such as:

- Attendance records
- Subjects
- Timetable configuration
- Bunk Bank information
- Attendance-related settings

The local-first design means that the core attendance functionality does not depend on a remote attendance server.

---

## Local-First Design

BunkVerse does not require:

- User accounts
- Cloud attendance storage
- Continuous internet connectivity

Core application data remains on the user's device.

Internet connectivity is primarily required for external services such as advertisements.

---

## Serialization

Gson is used for JSON serialization and deserialization where required by the application.

This allows structured application data to be converted between Java objects and JSON representations.

---

## User Interface

BunkVerse uses Android Material Components for its interface.

The application follows a futuristic dark HUD-inspired visual style.

Key visual characteristics include:

- Dark background
- Cyan accent system
- Glass-style UI components
- HUD-inspired information displays
- Animated elements
- Visual attendance indicators

---

## Animation

Lottie is used for application animations.

This allows animated visual elements to be integrated into the interface without requiring the animations to be manually implemented frame by frame.

---

## Tutorial System

BunkVerse includes a built-in tutorial system.

The tutorial is stored locally in Markdown format.

The application workflow is:

```text
tutorial.md
     ↓
Markdown Processing
     ↓
HTML
     ↓
Styled WebView
     ↓
In-App Tutorial
