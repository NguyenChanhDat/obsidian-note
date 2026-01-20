---
topic: 
date: "2026-01-20"
course: 
tags:
  - studies
---

# Etag

## Key Concepts

An _ETag_ value is an opaque string token that a server associates with a resource to uniquely identify the state of the resource over its lifetime.

If the resource at a given URL changes, a new `Etag` value _must_ be generated. A comparison of them can determine whether two representations of a resource are the same.

While requesting a resource, client sends the _ETag_ in _If-None-Match_ header field to the server. The server matches the _Etag_ of the requested resource and the value sent in _If-None-Match_ header. If both values match the server sends back a `304` `Not Modified` status, without a body, which tells the client that the cached version of the response is still good to use (_fresh_).

```bash
ETag: "abcd1234567n34jv"
```

## References

https://restfulapi.net/caching/
## Related Topics
- [[caching]]
- [[REST API]]