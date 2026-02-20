---
layout: default
title: Code Review
---

# Code Review

Video
[Open Code Review Video (SharePoint)](https://snhu-my.sharepoint.com/:v:/r/personal/ivan_isip_snhu_edu/Documents/SNHU/Term%201/CS499/Module%202/submit/Module%202%20-%20Milestone%20One-%20Code%20Review.mp4?csf=1&web=1&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=xXBigK)

Preview
[![Code Review Video Preview](images/APP_01_login_success.png)](https://snhu-my.sharepoint.com/:v:/r/personal/ivan_isip_snhu_edu/Documents/SNHU/Term%201/CS499/Module%202/submit/Module%202%20-%20Milestone%20One-%20Code%20Review.mp4?csf=1&web=1&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=xXBigK)

Summary
This code review covers my Android Event Tracker app. The video starts with an app demo, then reviews code issues tied to maintainability, data handling, database reliability, and security. The video explains planned fixes across software design, algorithms and data handling, and databases.

Timestamps
00:00 Intro  
00:25 App demo  
02:04 Software design review begins  
03:25 Software design issues found  
07:17 Planned fixes for software design and app flow  
10:41 Database review and CRUD overview  
13:58 Database issues and planned fixes  
18:40 Close  

What I reviewed
Software design and engineering
- AndroidManifest exported flags on internal activities
- SharedPreferences key mismatch across activities
- Logout flow leaving stored session data
- Change password flow missing old password validation
- Duplicate navigation logic across classes
- Duplicate SMS permission and sending logic

Algorithms and data handling
- Input validation for event fields
- Event list behaviors for search, filter, sort, and empty results
- Consistent formatting of event list output

Databases
- SQLite schema for Users and Events
- Parameterized queries for login and event retrieval
- CRUD operations for events
- Schema upgrades without losing existing data
- Indexes to support sort and filter performance
