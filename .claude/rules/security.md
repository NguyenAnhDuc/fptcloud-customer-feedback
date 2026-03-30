# Security Rules

- All endpoints require authentication (FPT ID JWT)
- Validate JWT on every request via middleware
- No hardcoded secrets — use environment variables
- Rate limit feedback submission (max 10/hour per user)
- Sanitize all text inputs before storing
