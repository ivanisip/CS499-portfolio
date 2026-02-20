---
layout: page
title: Enhancement 3 Databases
---

Purpose and user problem  
Users need reliable storage for accounts and events. Data needs to persist across app updates. Queries need stable ordering and performance support.

Original database state  
The database stored users and events but needed stronger version control, safer upgrade handling, and performance support for list operations.

Database enhancements  
- Controlled schema changes through DB_VERSION  
- Added safe upgrade logic to preserve existing data  
- Added indexes for common lookups  
- Used parameterized queries for authentication and event retrieval  
- Kept full CRUD operations for events

Evidence  
Database version  
<img src="{{ '/images/db-version.png' | relative_url }}" alt="DB version" style="max-width: 900px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

Schema create  
<img src="{{ '/images/db-schema-create.png' | relative_url }}" alt="Schema create" style="max-width: 900px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

Upgrade logic  
<img src="{{ '/images/db-upgrade-logic.png' | relative_url }}" alt="Upgrade logic" style="max-width: 900px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

Indexes  
<img src="{{ '/images/db-indexes.png' | relative_url }}" alt="Indexes" style="max-width: 900px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

Parameterized auth query  
<img src="{{ '/images/db-auth-query.png' | relative_url }}" alt="Auth query" style="max-width: 900px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

Parameterized event query  
<img src="{{ '/images/db-event-query.png' | relative_url }}" alt="Event query" style="max-width: 900px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

CRUD insert  
<img src="{{ '/images/db-crud-insert.png' | relative_url }}" alt="CRUD insert" style="max-width: 900px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

CRUD update and delete  
<img src="{{ '/images/db-crud-update-delete.png' | relative_url }}" alt="CRUD update delete" style="max-width: 900px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

Upgrade evidence  
Before version bump  
<img src="{{ '/images/up-before-version-bump.png' | relative_url }}" alt="Before version bump" style="max-width: 900px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

DB version 13  
<img src="{{ '/images/up-db-version-13.png' | relative_url }}" alt="DB version 13" style="max-width: 900px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

After version bump  
<img src="{{ '/images/up-after-version-bump.png' | relative_url }}" alt="After version bump" style="max-width: 900px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">

DB version 14  
<img src="{{ '/images/up-db-version-14.png' | relative_url }}" alt="DB version 14" style="max-width: 900px; width: 100%; height: auto; border: 1px solid #ddd; border-radius: 8px;">