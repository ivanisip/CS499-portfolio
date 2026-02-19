---
layout: page
title: Enhancement 2 Algorithms and Data Structures
---

# Enhancement 3 Databases

Purpose and user problem  
Users need reliable storage for accounts and events. Data must persist across app updates. Queries must stay safe and predictable. The event list needs stable ordering and performance support.

Original database state  
The database stored users and events but needed stronger version control, upgrade handling, and performance support for list operations.

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
![DB version](images/DB_01_VERSION.png)

Schema create  
Users and Events tables created with created_at.  
![Schema create](images/DB_02_Schema_create.png)

Upgrade logic  
onUpgrade adds created_at and preserves data.  
![Upgrade logic](images/DB_03_upgrade_logic.png)

Indexes  
Indexes added for faster filtering and sorting.  
![Indexes](images/DB_04_indexes.png)

Parameterized auth query  
Login uses a parameterized query.  
![Auth query](images/DB_05_parameterized_auth_query.png)

Parameterized event query  
Event retrieval uses parameters and stable ordering.  
![Event query](images/DB_06_parameterized_event_query.png)

CRUD write  
Insert event stores created_at.  
![CRUD write](images/DB_07_crud_write.png)

CRUD update and delete  
Update and delete operate by event id.  
![CRUD update delete](images/DB_07B_crud_update_delete.png)

Result  
The database preserves user and event data across version changes, supports predictable ordering, and improves query performance while keeping queries safer through parameter binding.