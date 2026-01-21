---
topic: 
date: "2026-01-21"
course: 
tags:
  - studies
---

# http2_core_strength

## Key Concepts

### Request Response Multiplexing

Trong HTTP/1, cụ thể là Pipelining, khi client muốn tối ưu connection bằng cách thực hiện nhiều request một lượt rồi đợi response trả về. Điểm hạn chế chúng ta đã biết response phải đúng thứ tự so với request. Việc này gây hiện tượng HOL.

Để khắc phục việc này, HTTP/2 sử dụng Multiplexing cho cả Request và Response. Có thể tạm hiểu rằng chúng được định danh để biết được response nào của request nào. Từ đó chúng có thể hoạt động độc lập mà không cần tuân thủ thứ tự như trước.
## References

- https://200lab.io/blog/http2-la-gi
## Related Topics
- [[http]]
- [[REST API]]