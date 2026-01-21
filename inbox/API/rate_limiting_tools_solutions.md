---
topic:
date: 2026-01-21
course:
tags:
  - studies
---


# rate_limiting_tools_solutions

## Key Concepts

![[Pasted image 20260121110556.png]]

## Examples

## pi gateway rate limiting (azure api management)

This is **more intelligent** than CDN, but still sits **in front of your backend**.

`client → api gateway → backend service`
## how azure api management counts rate

### where is the counter stored?

➡️ **inside Azure APIM’s internal distributed store**

You **do not manage it**.  
No Redis setup.  
No DB schema.  
Azure handles consistency & scale.
### what can Azure APIM count by?

Very flexible — examples:
- subscription key
- user ID (JWT claim)
- IP address
- API
- operation
- custom header
- combination of the above
## example: real APIM rate-limit policy

``` xml
<rate-limit-by-key    calls="100"    renewal-period="60"   counter-key="@(context.Subscription.Key)" />
```

Meaning:
- 100 calls
- per 60 seconds
- per **subscription key**
Azure internally does:
`counter["sub_abc123"] += 1`

### per-user rate limiting (JWT-based)

``` xml
<rate-limit-by-key    calls="20"   renewal-period="60"   counter-key="@(context.Request.Headers.GetValueOrDefault("Authorization",""))" />
```

or better:

`counter-key="@(context.Principal?.Claims["sub"]?.Value)"`

Now you’re limiting:  
➡️ **per authenticated user**

## real-world Azure setup (very common)

```
client   
↓ cloudflare / front door (IP throttling)   
↓ azure api management (user & subscription rate limits)   
↓ backend services
```

Why both?

- CDN blocks floods
- APIM enforces **fair usage**
## References

- https://restfulapi.net/rest-api-rate-limit-guidelines/
## Related Topics
- [[REST API]]