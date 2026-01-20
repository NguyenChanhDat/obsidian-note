---
topic: 
date: "2026-01-20"
course: 
tags:
  - studies
---

# hypermedia

# Conclusion

You **Shouldn't give a shit about this**

### Key Concepts

It means data should somehow carry an address, link,. ... 
sometimes called **[[HATEOAS]]** (hypermedia as the engine of application state)

### Examples

``` json
{
  "id": 42,
  "name": "alice",
  "links": {
    "self": "/users/42",
    "posts": "/users/42/posts",
    "update": "/users/42",
    "delete": "/users/42"
  }
}

```
## References


## Related Topics
- [[REST API]]
- [[resource_indentifier]]
- [[six_principle_REST]]
- [[HATEOAS]]