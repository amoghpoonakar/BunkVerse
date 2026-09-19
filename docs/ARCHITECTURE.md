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

## ZUMI Assistant Architecture

ZUMI is implemented as a local assistant engine that works with the application's existing database and preferences.

The assistant receives a user's question, normalizes the text, identifies a supported intent, extracts relevant information such as a weekday or subject, and then reads the required data from BunkVerse.

The current supported intent categories include:

- Timetable
- Attendance
- Bunk check
- Bunk overview

ZUMI also maintains lightweight conversational context for clear follow-up questions.

The context can include:

- Last referenced day
- Last referenced subject
- Last detected intent

This context is intentionally limited so that an old subject or intent is not incorrectly reused for unrelated questions.

### ZUMI Data Flow

```text
User Question
      ↓
Text Normalization
      ↓
Conversation Handling
      ↓
Intent Detection
      ↓
Subject / Day Extraction
      ↓
Application Database & Preferences
      ↓
Response Generation
      ↓
ZUMI Response
```

### Timetable Integration

For timetable questions, ZUMI reads timetable entries from the local database, orders them by start time, and resolves subject short codes to full subject names where available.

Lunch entries are excluded from the returned class list.

### Attendance Integration

For attendance questions, ZUMI reads stored attendance records and calculates the requested subject or overall logged attendance from those records.

### Bunk Bank Integration

For bunk questions, ZUMI uses `BunkBankCalculator` and its monthly statistics rather than maintaining a separate bunk calculation system.

The monthly statistics include:

- Total classes
- Available bunks
- Used bunks
- Medical leaves
- Remaining bunks
- Passed-month state

Remaining bunks are derived from the Bunk Bank data as:

```text
Remaining Bunks = Available Bunks - Used Bunks
```

ZUMI therefore uses the same Bunk Bank calculation source as the application's bunk-management system.

### Natural-Language Handling

ZUMI supports common variations of supported requests instead of requiring one exact command.

Examples include:

- "Can I bunk DBMS?"
- "Can I skip OS?"
- "Can I miss class?"
- "What classes can I bunk this month?"
- "How many bunks are left?"

It also handles basic greetings, thanks, goodbyes, help requests, and selected conversational follow-ups.

Unsupported requests receive a development response instead of a guessed answer.

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
```

---

## Future Architecture Improvements

Potential future architectural improvements include:

- Expanding ZUMI's supported intents
- More advanced conversational context
- Deeper integration between ZUMI and application features
- Additional analytics and planning services
- Further separation of assistant logic from UI components
- More modular feature-specific services

ZUMI is intended to remain grounded in BunkVerse's own application data rather than maintaining an independent copy of attendance or Bunk Bank state.
