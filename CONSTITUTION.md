# CONSTITUTION.md — Cross-repo API Contract

> This file is frozen after Day 3 sign-off. Changes require Dev Lead approval.

## API Base
- Base URL: `http://localhost:5000/api/v1` (dev)
- Production: `https://console-api.fptcloud.com/api/v1`

## Feedback Endpoints

### Submit feedback
POST /api/v1/feedback
Request:
```json
{
  "page_path": "/compute/instance",
  "rating": 4,
  "comment": "Optional free text",
  "user_id": "uuid"
}
```
Response 201:
```json
{
  "id": "uuid",
  "created_at": "ISO8601"
}
```
Error 400: `{"error": "VALIDATION_ERROR", "message": "..."}`

### Get feedback stats (admin)
GET /api/v1/feedback/stats?page_path=&from=&to=
Response 200:
```json
{
  "avg_rating": 4.2,
  "total": 150,
  "by_rating": {"1": 5, "2": 10, "3": 20, "4": 60, "5": 55}
}
```

### List feedback (admin)
GET /api/v1/feedback?page=1&limit=20&page_path=
Response 200:
```json
{
  "items": [...],
  "total": 150,
  "page": 1,
  "limit": 20
}
```

## Auth
- All admin endpoints require: `Authorization: Bearer <FPT_ID_JWT>`
- Submit endpoint: authenticated users only

## Error format (ALL endpoints)
```json
{"error": "ERROR_CODE", "message": "Human readable"}
```
Error codes: VALIDATION_ERROR, UNAUTHORIZED, NOT_FOUND, INTERNAL_ERROR

## NEVER
- NEVER use FastAPI — this project uses Flask 3.x exclusively
- NEVER return raw exceptions to client
- NEVER skip input validation
