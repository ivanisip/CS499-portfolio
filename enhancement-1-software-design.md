---
layout: page
title: Enhancement 1 Software Design and Engineering
---

# Enhancement 1 Software Design and Engineering

Purpose and user problem  
Users need a clear, consistent app flow for login, navigation, and account management. The app must protect internal screens from being launched outside the app and keep session behavior predictable.

Original state  
The app worked end to end but had design issues that increased maintenance work and created security gaps. Some internal activities allowed external launch through the manifest. SharedPreferences usage also risked mismatched reads across screens.

Enhancements implemented  
- Locked down internal activities by setting exported false for non-entry screens  
- Standardized SharedPreferences usage for the signed-in username  
- Ensured logout clears the saved signed-in user  
- Reduced duplicate navigation logic by keeping one navigation implementation

Evidence  
Add screenshots in this section from your code and emulator runs.

- Manifest exported settings: images/ADD_FILE.png  
- SharedPreferences key usage: images/ADD_FILE.png  
- Logout clearing preferences: images/ADD_FILE.png  
- Navigation flow screenshots: images/APP_02_home.png

Result  
Users move through login, home, events, and account screens with predictable navigation. Internal screens stay protected, and logout removes session state.