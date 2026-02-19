---
layout: default
title: Professional Self-Assessment
---

# Professional Self-Assessment

## Professional identity
My goal is a software role focused on mobile and internal business tools. I built an Android Event Tracker app in Java with SQLite storage. I designed features around fast entry, quick lookup, and reliable edits. I improved maintainability by removing duplicated logic and standardizing shared preferences for session state. I improved list handling by adding search, room filtering, and sorting with accurate shown counts. I improved database reliability through schema versioning, safe upgrades, indexes, and parameterized queries. This portfolio shows how I build, test, document, and publish software in a maintainable way.

## Program outcomes with evidence

### Outcome 1 Collaborative environments and decision support
I translated user needs into features such as create, view, edit, delete, and room context. I made design choices with clear trade-offs, such as local storage for speed and offline use. I documented decisions through enhancement narratives and evidence screenshots tied to behavior and code.

### Outcome 2 Professional oral, written, and visual communication
I produced a code review video showing a demo, key findings, and planned changes across the three categories. I wrote enhancement narratives with purpose, changes, skills, trade-offs, and security impact. I publish visuals in this ePortfolio, including UI flows, database code, upgrade logic, and query patterns.

### Outcome 3 Algorithmic design with trade-offs
I implemented search, room filters, and sort options for the event list. I show total records and shown records to support decisions during filtering. I use stable ordering for consistent results, then support performance with ordering and indexes.

### Outcome 4 Tools, techniques, and implementation value
I use Android Studio, emulator testing, and Git version control to build and validate features. I apply SQLiteOpenHelper patterns for schema creation, versioning, and safe upgrades. I publish this ePortfolio through GitHub Pages with clear navigation and run steps.

### Outcome 5 Security mindset
I store passwords as hashes and verify credentials using parameterized queries. I block password changes when old password validation fails. I clear session state during logout and avoid storing unnecessary sensitive data.

## Growth and next steps
- Add automated tests for database upgrades and query results
- Add stricter field validation for event name, room name, and guest ranges
- Add stronger password rules and consistent error messages
- Add export or backup for event data
- Add accessibility checks for text size and contrast