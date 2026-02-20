---
layout: default
title: Enhancement 3 Databases
---

Enhancement 3 Databases

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
![DB version](images/db-version.png)

Schema creation
![DB schema create](images/db-schema-create.png)

Upgrade logic
![DB upgrade logic](images/db-upgrade-logic.png)

Indexes
![DB indexes](images/db-indexes.png)

Parameterized queries
![DB auth query](images/db-auth-query.png)
![DB event query](images/db-event-query.png)

CRUD writes
![DB CRUD insert](images/db-crud-insert.png)
![DB CRUD update delete](images/db-crud-update-delete.png)

Upgrade evidence screenshots
![Before version bump](images/up-before-version-bump.png)
![After version bump](images/up-after-version-bump.png)
![DB version 13](images/up-db-version-13.png)
![DB version 14](images/up-db-version-14.png)