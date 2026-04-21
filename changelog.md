## 2026-04-21 13:38:24 +0700

- Fixed slider deletion error by correcting `sliderAPI.delete()` to call the `/api/slider/:id` endpoint (previously hit the non-API `/slider/:id` route and could return non-JSON/404 responses).

