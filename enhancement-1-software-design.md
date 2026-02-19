---
layout: default
title: Enhancement 1
---

# Enhancement 1 Software Design and Engineering

Purpose and user problem  
Users need a simple event workflow with reliable navigation and consistent account behavior. The app must keep session state consistent across screens and block unsafe credential changes.

Original state  
The app worked, but session state handling and credential change behavior needed tighter consistency and safer validation.

Enhancement work  
- Standardized session storage so screens read the same saved username  
- Improved navigation flow using a consistent home path  
- Added safer credential change behavior by validating old password

Skills demonstrated  
- Refactoring for maintainability  
- Consistent state management  
- Input validation and safer authentication flow  
- UI verification through emulator testing

Evidence  
Login screen  
![Login](images/login.png)

Home screen  
![Home](images/home.png)

Create event screen  
![Create event](images/create-event.png)

Account info screen  
![Account info](images/account-info.png)

Change password blocks incorrect old password  
![Old password incorrect](images/change-password-old-wrong.png)

Trade-offs  
I chose shared preferences session storage for speed and clarity. This keeps implementation small and easy to maintain.

Security  
I validate old password during password changes and avoid weak flows that allow silent updates.

How to run  
1 Install and run in Android Studio.  
2 Register a user.  
3 Login, open Account, and confirm account details display.  
4 Try Change Password using a wrong old password and confirm it blocks the change.