---
layout: page
title: Enhancement 3 Databases
---

# Enhancement 3 Databases

Purpose and user problem  
Users need reliable storage for accounts and events. Data must persist across app updates. Queries must stay safe and predictable. The event list needs stable ordering and performance support.

Original database state  
The database stored users and events, but needed stronger version control, upgrade handling, and performance support for list operations.

Database enhancements  
- Controlled schema changes through DB_VERSION  
- Added created_at for stable ordering  
- Added safe onUpgrade logic to preserve existing data  
- Added indexes for created_at, room, and name  
- Used parameterized queries for authentication and event retrieval  
- Kept full CRUD operations for events

Evidence  

Database version  
DB_VERSION set for controlled schema upgrades.  
![DB version](images/db-version.png)

Schema proof  
Users and Events tables include required fields. Events includes created_at.  
![Schema create](images/db-schema-create.png)

Upgrade proof  
onUpgrade adds created_at for older installs and backfills values for existing rows.  
![Upgrade logic](images/db-upgrade-logic.png)

Before version bump  
![Before version bump](images/up-before-version-bump.png)

DB version 13 baseline  
![DB version 13](images/up-db-version-13.png)

DB version 14 after bump  
![DB version 14](images/up-db-version-14.png)

After version bump with data still visible  
![After version bump](images/up-after-version-bump.png)

Index proof  
Indexes support sort and filter performance for created_at, room, and name.  
![Indexes](images/db-indexes.png)

Parameterized authentication query  
Login uses selection arguments for username and hashed password.  
![Auth query](images/db-auth-query.png)

Parameterized event query and ordering  
Event queries use selection arguments and stable ordering.  
![Event query](images/db-event-query.png)

CRUD proof in code  
Insert writes name, value, room, and created_at.  
![CRUD insert](images/db-crud-insert.png)

Update and delete target a single row by id.  
![CRUD update and delete](images/db-crud-update-delete.png)

CRUD proof in UI  
Event details view  
![Event details](images/event-details.png)

Edit before update  
![Edit before](images/edit-before.png)

Edit after update  
![Edit after](images/edit-after.png)

Delete before  
![Delete before](images/delete-before.png)

Delete after  
![Delete after](images/delete-after.png)

How to run  
1 Create several events.  
2 View Events and confirm stable ordering by newest.  
3 Edit an event and confirm it updates.  
4 Delete an event and confirm it disappears.  
5 Bump DB_VERSION and confirm events still display.
