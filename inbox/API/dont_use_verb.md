---
topic: 
date: "2026-01-20"
course: 
tags:
  - studies
---


## Key Concepts

Don't use verb in naming URI's, that's RPC

## Important Details

Don't falling to stupid shit thing like, API has specific name for change a attribute of something
for instance update a status of seat in fly booking:

```json
/fly-management/sit-booking-management/planes/{planeId}/seats/{seatId}/update
```
==> This isn't REST, it's RPC
instead, by using POST method do this:

```json
PATCH /planes/{planeId}/seats/{seatId}
```
body:
```json
{ 
	"isAvailable":true
}
```
## Examples


## References


## Related Topics
- [[REST API]]
- [[API design principals]]
- [[naming_URIs]]