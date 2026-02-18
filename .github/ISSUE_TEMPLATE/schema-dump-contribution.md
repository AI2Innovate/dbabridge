---
name: Schema Dump Contribution
about: Share an anonymised schema for testing the DBA Bridge audit and migration engine.
title: "[SCHEMA] "
labels: test-data, contribution
assignees: ''
---

## Thank You

Schema dumps from real migration projects are the single most valuable testing material we have.  
Even a small schema with a few stored procedures helps validate the audit engine before launch.

---

## Schema Details

- Source database type and version: (e.g. Oracle 12c, SQL Server 2016)
- Intended target: (e.g. PostgreSQL 15, Supabase)
- Approximate size: (e.g. 15 tables, 8 stored procedures, 4 triggers)
- Was this migration ever attempted? (yes / no / in progress)
- If yes, what broke?

---

## Anonymisation Checklist

Before sharing, please confirm:

- [ ] All real table and column names replaced with fictional equivalents
- [ ] All real stored procedure logic replaced or removed (structure only is fine)
- [ ] No real data included — DDL only
- [ ] No connection strings, credentials, or server names included
- [ ] No proprietary business logic that should not be public

---

## The Schema

Paste the anonymised DDL here, or attach a `.sql` file.

```sql
-- paste your anonymised schema here
```

---

## Anything Specific to Test?

Are there particular data type conversions, stored procedure patterns, or FK structures you want us to handle correctly?

---

## Contact (Optional)

If you'd prefer to share privately rather than on a public issue:  
Email: info@ai2innovate.io  
Discord: [discord.gg/K64U65je7h](https://discord.gg/K64U65je7h)
