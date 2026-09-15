# Bunk Bank

The Bunk Bank is the core attendance-planning system developed for BunkVerse.

Instead of treating attendance as only a percentage, BunkVerse represents attendance flexibility through available bunks.

---

## Concept

Traditional attendance tracking answers:

> "What is my attendance percentage?"

BunkVerse additionally aims to answer:

> "How much attendance flexibility do I have?"

The Bunk Bank is designed around this second question.

---

## Available Bunks

Available Bunks represents the number of classes that can be missed while maintaining the configured attendance requirement.

The available amount changes as attendance records change.

---

## Bunk Pass

Bunk Pass allows unused bunks from a completed month to be carried into the next month.

### Purpose

Without a carry-forward mechanism, unused attendance flexibility would effectively disappear when a month ends.

Bunk Pass allows that unused flexibility to remain available for future planning.

---

## Bunk Loan

Bunk Loan allows bunks to be borrowed from future months.

### Purpose

There may be situations where a student needs more attendance flexibility than the current month provides.

Instead of manually altering attendance calculations, BunkVerse records the borrowed amount through the Bunk Bank system.

Borrowed bunks remain associated with their original source months.

---

## Medical Leave

Medical Leave allows eligible past absences to be converted so they no longer affect the relevant attendance calculation.

This operation is recorded within the Bunk Bank system.

---

## Undo

BunkVerse provides undo functionality for recent Bunk Loan and Medical Leave operations.

This allows users to correct accidental changes without manually reconstructing the previous state.

---

## Ledger

The Bunk Bank maintains a monthly ledger of attendance flexibility.

The ledger keeps track of operations such as:

- Bunk Pass
- Bunk Loan
- Medical Leave

This provides a structured history of how attendance flexibility has been used.

---

## Ledger Reset

A month can be completely reset through the Ledger Reset functionality.

When borrowed bunks are present, the reset process automatically returns them to their original source months.

This prevents borrowed attendance flexibility from permanently altering future monthly allocations.

---

## Responsible Attendance Planning

The Bunk Bank is not intended to encourage irresponsible attendance.

Its purpose is to make attendance calculations easier to understand and help students make informed decisions.

The philosophy behind the system is:

> **The goal isn't just to bunk; it's to plan your adventures without losing your attendance.**
