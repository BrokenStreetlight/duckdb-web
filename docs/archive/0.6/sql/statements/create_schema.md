---
expanded: SQL
layout: docu
railroad: statements/createschema.js
redirect_from:
- docs/archive/0.6.1/sql/statements/create_schema
selected: Documentation/SQL/Create Schema
title: Create Schema
---

The `CREATE SCHEMA` statement creates a schema in the catalog. The default schema is `main`.

### Examples
```sql
-- create a schema
CREATE SCHEMA s1;
-- create a schema if it does not exist yet
CREATE SCHEMA IF NOT EXISTS s2;
-- create table in the schemas
CREATE TABLE s1.t(id INTEGER PRIMARY KEY, other_id INTEGER);
CREATE TABLE s2.t(id INTEGER PRIMARY KEY, j VARCHAR);
-- compute a join between tables from two schemas
SELECT * FROM s1.t s1t, s2.t s2t WHERE s1t.other_id = s2t.id;
```

### Syntax
<div id="rrdiagram"></div>