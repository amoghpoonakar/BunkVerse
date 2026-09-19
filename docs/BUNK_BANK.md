# BunkVerse Features

This document provides a detailed overview of the features available in BunkVerse.

---

## 1. Bunk Bank

The Bunk Bank is the central concept behind BunkVerse.

Instead of requiring students to manually calculate how many classes they can miss, BunkVerse represents attendance flexibility through a system of available bunks.

### Available Bunks

Available Bunks represents the number of classes a student can safely miss while maintaining the configured attendance requirement.

The calculation is based on the student's attendance data and required attendance percentage.

The Bunk Bank also tracks used bunks and calculates remaining bunks from the current monthly allocation.

### Bunk Pass

Unused bunks from a completed month can be carried forward into the following month.

This allows unused attendance flexibility to be retained rather than discarded.

### Bunk Loan

Bunk Loan allows students to borrow available bunks from future months when additional flexibility is required.

Borrowed bunks are tracked through the Bunk Bank ledger.

### Medical Leave

Eligible past absences can be converted into medical leave so that they no longer affect the relevant attendance calculation.

### Undo

Recent Bunk Loan and Medical Leave operations can be reversed when an entry was made incorrectly.

### Ledger Reset

A monthly ledger can be completely reset.

When a ledger containing borrowed bunks is reset, borrowed bunks are automatically returned to the months from which they originally came.

---

## 2. ZUMI — Built-in Student Assistant

ZUMI is BunkVerse's built-in local assistant.

ZUMI provides a natural-language interface for supported timetable, attendance, and Bunk Bank information.

### Timetable Questions

Users can ask ZUMI about their schedule, including:

- Today's classes
- Tomorrow's classes
- A named weekday
- Weekly timetable information

### Attendance Questions

ZUMI can answer supported attendance questions for:

- Individual subjects
- Overall logged attendance

Subject names can be identified using the configured full subject name or short code.

### Bunk Questions

ZUMI can answer supported bunk-management questions such as:

- Whether a subject can be bunked on a particular day
- How many bunks remain
- Which subjects still have bunks available this month
- How many classes can still be bunked

For these answers, ZUMI reads Bunk Bank information from the application's Bunk Bank calculator.

### Natural Language

ZUMI supports common variations of student phrasing, including questions such as:

- "Can I bunk DBMS?"
- "Can I skip OS?"
- "Can I miss class?"
- "How many bunks are left?"
- "What classes can I bunk this month?"

The assistant also supports basic conversational follow-ups such as "what about tomorrow?" and "and today?".

### Voice Input

ZUMI can receive text produced through Android speech recognition, allowing users to ask supported questions using voice input.

### Supported Conversation

ZUMI also handles basic conversational interactions such as:

- Greetings
- Thanks
- Goodbyes
- Help requests

Unsupported requests receive a development response rather than an invented answer.

---

## 3. Attendance Tracking

BunkVerse provides calendar-based attendance management.

### Attendance States

A day can be recorded as:

- Full Day Present
- Absent
- Partial Attendance

Partial attendance allows individual subjects to be selected based on attendance for that particular day.

### Attendance Indicators

The calendar uses three visual states:

- 🟢 Green — Safe
- 🟡 Yellow — Caution
- 🔴 Red — Danger

### Non-Attendance Days

BunkVerse can account for days that should not affect attendance calculations, including:

- Sundays
- Holidays
- Examination days

### Date Range Selection

Users can long-press and select a range of dates to apply attendance-related changes across multiple days.

This is particularly useful for:

- Holidays
- Examination periods
- Multiple-day updates
- Clearing previously entered attendance

### Cancelled Classes

Individual scheduled classes can be removed from a particular day when a class is cancelled.

### Extra Classes

Classes outside the normal timetable can be added to a particular day.

---

## 4. Saturday & Weekend Support

BunkVerse supports different approaches to weekend scheduling.

Users can:

- Copy a timetable from any weekday to Saturday.
- Create a custom half-day Saturday timetable.
- Record attendance for weekend classes.

This allows the application to adapt to different college schedules.

---

## 5. Timetable Management

BunkVerse provides a customizable weekly timetable.

### Automatic Class Timing

Class end times are calculated automatically based on the configured duration of each subject.

### Lunch Breaks

Lunch breaks can be configured separately for each day.

The timetable automatically accounts for these breaks when generating the daily schedule.

### Subject Short Codes

Subjects can have short codes for display purposes.

For example:

`Database Management Systems`

can be represented in the interface using:

`DBMS`

The full subject name is retained internally.

---

## 6. Attendance Reports

Attendance reports can be generated for different periods.

### Available Periods

- Entire Semester
- Individual Month
- Custom Date Range

### Subject Filtering

Reports can display:

- All subjects
- A specific subject

### Attendance Categories

- 🟢 75% or above — Safe
- 🟡 60–74% — Caution
- 🔴 Below 60% — Danger

---

## 7. Local-First Storage

BunkVerse stores its core application data locally on the user's device.

This includes:

- Attendance records
- Subjects
- Timetable configuration
- Bunk Bank information
- Application settings

ZUMI uses this locally available application data for its supported timetable, attendance, and Bunk Bank responses.

No account is required to use the core attendance-management functionality.

---

## 8. Backup

BunkVerse provides CSV-based data export.

The generated file is:

`BunkVerse_Backup.csv`

The exported data can include:

- Subjects
- Attendance records
- Timetable information
- Bunk Bank data
- Application settings

The backup provides users with a personal copy of their application data.

---

## 9. Built-in Tutorial

BunkVerse includes a tutorial stored as a local Markdown file.

The application:

1. Reads the Markdown content.
2. Converts it into HTML.
3. Displays the resulting content inside a styled WebView.

This keeps the tutorial integrated into the application.

---

## 10. Complete Reset

BunkVerse includes a complete reset function.

The reset clears the application's locally stored database and preferences, returning the application to a fresh-install state.

---

## 11. Advertising

BunkVerse uses Google AdMob for banner advertisements.

The core attendance-management functionality is designed to operate locally without requiring a constant internet connection.

Internet connectivity may be required for advertisement-related services.

---

## 12. Room for Improvement

BunkVerse is actively evolving, and the following areas can be expanded in future versions.

### ZUMI Improvements

Potential ZUMI improvements include:

- More advanced conversational context
- More complex multi-step questions
- Better follow-up understanding
- More detailed attendance analysis
- More detailed Bunk Bank explanations
- More flexible date and time interpretation
- Expanded voice interaction
- Additional supported application actions
- Deeper integration with more BunkVerse features
- More personalized student workflows

### Bunk Bank Improvements

Potential improvements include:

- More detailed monthly planning
- Additional bunk-management insights
- Expanded carry-forward functionality
- Improved bunk usage visualization
- More detailed historical analysis

### Attendance & Analytics Improvements

Future versions can provide additional attendance trends, analysis, and planning tools.

### User Experience Improvements

Potential improvements include:

- Faster attendance logging
- More streamlined timetable management
- Improved report visualization
- Additional customization options
- Improved onboarding and tutorials
