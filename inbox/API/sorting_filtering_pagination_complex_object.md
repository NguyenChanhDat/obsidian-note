---
topic: 
date: "2026-01-21"
course: 
tags:
  - studies
---

# sorting_filtering_pagination_complex_object

## Key Concepts

### common REST compromises

#### ✅ simple filters → query params

`?author=foo&year=2024`

#### ✅ complex search → POST

``` json
POST /api/books/search {   
	"filters": {     
		"authors": ["foo", "bar"],     
		"price": { "min": 10, "max": 100 },
	},   
	"sort": [     
		{ 
			"field": "author", 
			"direction": "ASC" 
		}   
	] 
}
```

this is **very common in real projects**. It just like **GraphQL**

---

## 7️⃣ why POST for search is acceptable in REST

because:
- it’s no longer a “simple retrieval”
- request is complex
- caching is less important
- body is easier to evolve
many large REST APIs do this.

important note:

> this is **REST-inspired**, not “pure REST”

and that’s okay.

---

## 8️⃣ why REST didn’t adopt GraphQL-style bodies

because REST predates GraphQL by decades and was designed around:
- browsers
- proxies
- CDNs
- HTTP caching
- bookmarks
- curl

GraphQL was designed around:
- typed clients
- single endpoint
- application-level caching

different constraints → different design.

---

## 9️⃣ real-world rule of thumb (very practical)

|case|recommended|
|---|---|
|simple list|GET + query params|
|sortable table|GET + query params|
|public api|GET + query params|
|complex filtering|POST /search|
|graphql-like flexibility|GraphQL|

---

## 10️⃣ your instinct is actually correct

> “throwing everything in the body feels cleaner”

yes — **for application developers**.

but REST optimizes for:
- infrastructure
- tooling
- visibility
- cacheability

not just developer ergonomics.

---

## one-sentence takeaway

> **REST puts “how to view data” in the URL because the web itself understands URLs; GraphQL puts it in the body because the application understands the query**
## Related Topics
- [[REST API]]
