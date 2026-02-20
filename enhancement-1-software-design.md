---
layout: page
title: Enhancement 1 Software Design and Engineering
---

Purpose and user problem  
Users need a stable app flow across login, navigation, and event management screens. The code needs consistent session handling and reduced duplication to lower bug risk.

Original state  
I had repeated navigation logic across classes and inconsistent shared preferences keys across screens.

Enhancement work  
- Standardized shared preferences usage so screens read the same logged-in user value  
- Reduced duplicated navigation logic so updates happen in one place  
- Improved logout flow so sign-out clears stored session state

Evidence screenshots  
Account info  
<img src="{{ '/images/account-info.png' | relative_url }}" alt="Account info screen" style="max-width: 360px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

Change password validation example  
<img src="{{ '/images/change-password-old-wrong.png' | relative_url }}" alt="Change password wrong old password" style="max-width: 360px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

Create event  
<img src="{{ '/images/create-event.png' | relative_url }}" alt="Create event screen" style="max-width: 360px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">