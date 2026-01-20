---
topic: 
date: "2026-01-20"
course: 
tags:
  - studies
---

# idempotency

## Key Concepts

**idempotence** in programming means:

> calling an operation **multiple times** has the **same effect as calling it once**.

the **resulting state** does not change after the first successful call.
## Important Details


## Examples

idempotent operation:

``` sql
UPDATE users SET status = 'active' WHERE id = 1;
```

non-idempotent:

```sql
UPDATE users SET login_count = login_count + 1;
```

## References


## Related Topics
- [[REST API]]