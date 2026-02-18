---
name: Migration Bug Report
about: Something broke during or after your database migration. Tell us exactly what happened.
title: "[BUG] "
labels: bug, migration-edge-case
assignees: ''
---

## Migration Pair

What were you migrating between?

- Source database: (e.g. Oracle 19c, SQL Server 2019, MySQL 8.0)
- Target database: (e.g. PostgreSQL 15, Supabase)
- Tool you were using: (e.g. AWS DMS, Azure Migrate, ora2pg, pgloader, manual)

---

## What Broke

Describe what failed after migration. Be as specific as possible.

Examples:
- "Stored procedure `calculate_order_total` failed with error: `syntax error at or near 'ROWNUM'`"
- "Column `created_at` was Oracle DATE type. After migration it lost the time component."
- "Foreign key on `order_items.product_id` failed to re-enable — constraint violation on 3,412 rows"
- "App ORM (Hibernate) broke because column `user` is a reserved word in Postgres"

**Describe the bug:**


---

## Schema Context (Optional but very useful)

If you can share the relevant table/procedure structure (anonymised), paste it here.  
Even just the column names and types involved helps us build a test case.

```sql
-- paste anonymised schema here (replace real names with fictional ones)
```

---

## What the Tool Reported

What did the migration tool say? Did it report success despite the failure?

- [ ] Tool reported success but app broke
- [ ] Tool reported an error but no explanation of how to fix it
- [ ] Tool had no output at all
- [ ] Other:

---

## Impact

How much time did this cost you?

- [ ] Hours
- [ ] Days
- [ ] Weeks
- [ ] The migration was abandoned

---

## Additional Context

Anything else that would help us understand the problem.
