---
topic:
date: 2026-01-21
course:
tags:
  - studies
---
## Key Concepts

## what frontend deploy looks like (modern reality)

frontend deployment is **closer to publishing files** than running a server.

### step-by-step fe deploy

#### 1️⃣ build step (very important)

you run:

`npm run build`

this produces:

`/dist   
├─ index.html   
├─ assets/app.9fd23.js   
├─ assets/style.a12c.css`

➡️ **pure static files**  
➡️ no react, no node, no server logic anymore

---

#### 2️⃣ upload files to a static host

you upload `/dist` to one of these:
- Amazon S3 + CloudFront
- Vercel
- Netlify
- Nginx
- Azure Static Web Apps

these platforms:
- store files
- serve them over http
- cache them globally

---

#### 3️⃣ expose a url

you get:

`https://www.example.com`

when someone opens it:

`browser → GET /index.html host → returns file`

and that’s the **entire fe “server” job**.

---

## what happens at runtime (important)

after files are downloaded:

- react runs **inside the browser**
- routing is client-side
- state is per browser tab
- backend api is called separately

`browser (react)    ↓ https://api.example.com`

frontend host is **not involved anymore**.
## Important Details


## Examples


## References


## Related Topics
- [[Software_Concepts]]