---
layout: default
title: Enhancement 2
---

# Enhancement 2 Algorithms and Data Structures

Purpose and user problem  
Users need to find events fast. They need search by event or room, filter by room, and sort results, with clear counts and clear empty results feedback.

Original state  
The event list showed events, but needed stronger search, filter, sort, and clearer results feedback.

Enhancement work  
- Added text search over event name and room name  
- Added room filtering  
- Added sorting options including sorting by guest count  
- Added total and shown counts plus a no-results message

Algorithm and data structure details  
Data flow  
1 Load events from SQLite.  
2 Apply room filter when selected.  
3 Apply search filter on event name and room name.  
4 Apply sort order selection.  
5 Render results and update shown count.

Trade-off  
I kept logic readable and stable for the UI. I support performance with ordering and indexes in the database layer.

Evidence  
No results message and shown count reaches zero  
![No results](images/no-results.png)

Search filter returns a single match and updates shown count  
![Search filter](images/search-filter.png)

Room filter returns one room and updates shown count  
![Room filter](images/room-filter.png)

Sort by guests orders events by guest count  
![Sort by guests](images/sort-by-guests.png)

How to run  
1 Open View Events.  
2 Type a search term and verify shown count updates.  
3 Select a room and verify list filters.  
4 Change sort to Guests and verify ordering changes.