---
topic: 
date: "2026-01-21"
course: 
tags:
  - studies
---

# avoid_version_lock_promiscuity

## Key Concepts

### version lock (too strict → clients get stuck)

#### what it looks like in real life

**API design**

`GET /api/v1/orders GET /api/v2/orders GET /api/v3/orders`

#### what changed
- `v1` → returns `totalPrice`
- `v2` → renamed to `total_amount`
- `v3` → changed date format

Each version is **not backward compatible**.

## version promiscuity (too loose → undefined behavior)

Now the opposite problem.
### what it looks like

**API accepts versions like**

`GET /api/orders X-API-Version: 1 X-API-Version: 1.1 X-API-Version: latest X-API-Version: beta`

Backend logic:

`if (version >= 1.1) {   includeDiscounts(); }`

### what goes wrong

Client A sends:
`X-API-Version: 1`
Client B sends:
`X-API-Version: latest`
Client C sends nothing.

All of them:
- get **different responses**
- with **no clear contract**
- no guaranteed compatibility
### real symptoms

- “It worked yesterday, broke today”
- frontend and backend disagree on payload
- debugging depends on request headers
- support team can’t reproduce issues

👉 API becomes **unpredictable**

## References

- https://restfulapi.net/rest-api-best-practices/
## Related Topics
- [[API design principals]]
- [[REST API]]