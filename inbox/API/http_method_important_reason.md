---
topic: 
date: "2026-01-20"
course: 
tags:
  - studies
---

# http_method_important_reason

## Key Concepts

## then why do we care about http methods at all?

because http methods give you **free semantics**:

- caching (`GET`)
- idempotency (`PUT`, `DELETE`)
- safety (`GET`)
- tooling support

so while rest doesn’t _require_ them, **engineering best practice strongly prefers them**.
## Examples

### examples

- Cloudflare
- Fastly
- Akamai
- Varnish Cache

### what they assume

- `GET` → cacheable by default
- `POST` → **not cacheable**
- `PUT / DELETE` → invalidate or bypass cache
## References

- **rfc 9110 – http semantics**
    - sections 9.2, 9.3

- **rfc 9111 – http caching**

- **mdn web docs – http methods**
    - practical explanation for engineers 
## Related Topics
- [[REST API]]