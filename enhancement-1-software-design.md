---
layout: default
title: Enhancement 1 Software Design and Engineering
---

Enhancement 1 Software Design and Engineering

Purpose and user problem
Users need a clear flow from login to event creation and event review. The app needs consistent session handling and reduced duplicate logic to lower maintenance effort.

Original state
The app worked end to end, but some logic repeated across activities. Session data handling needed consistency across screens.

Enhancements
- Standardized session storage and retrieval across screens.
- Reduced duplicate navigation and shared logic.
- Kept screens focused on one job per activity.

Evidence

Login and navigation entry
![Login screen](images/login.png)
![Home screen](images/home.png)

Event flow
![Create event](images/create-event.png)
![Event details](images/event-details.png)

Edit and delete flow
![Edit before](images/edit-before.png)
![Edit after](images/edit-after.png)
![Delete before](images/delete-before.png)
![Delete after](images/delete-after.png)

Account and password screens
![Account info](images/account-info.png)
![Change password wrong old password](images/change-password-old-wrong.png)