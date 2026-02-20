---
layout: page
title: Enhancement 2 Algorithms and Data Structures
---

Purpose and user problem  
Users need fast ways to find events. The list needs predictable sorting and usable filtering to reduce time spent scrolling.

Original state  
Event list behavior depended on default query order and did not provide clear filtering feedback.

Enhancement work  
- Added sorting options aligned to user goals, such as sorting by guest count  
- Added filtering by room and search text  
- Kept list counts visible so users see total vs shown results

Evidence screenshots  
Search filter  
<img src="{{ '/images/search-filter.png' | relative_url }}" alt="Search filter" style="max-width: 360px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

Room filter  
<img src="{{ '/images/room-filter.png' | relative_url }}" alt="Room filter" style="max-width: 360px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

Sort by guests  
<img src="{{ '/images/sort-by-guests.png' | relative_url }}" alt="Sort by guests" style="max-width: 360px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

No results state  
<img src="{{ '/images/no-results.png' | relative_url }}" alt="No results state" style="max-width: 360px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">