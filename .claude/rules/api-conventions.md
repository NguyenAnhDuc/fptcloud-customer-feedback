# API Conventions

- Base path: `/api/v1/`
- All responses JSON
- Success: 200/201 with data object
- Error: always `{"error": "ERROR_CODE", "message": "..."}`
- Pagination: `?page=1&limit=20` → `{items, total, page, limit}`
- Datetime: ISO8601 strings
- IDs: UUID v4
- Auth header: `Authorization: Bearer <token>`
