# Error Handling

- NEVER expose raw exceptions to client
- Always return `{"error": "ERROR_CODE", "message": "Human readable"}`
- Use Flask error handlers for 400, 401, 404, 500
- Log exceptions server-side before returning generic error
- Validate all inputs before processing (use marshmallow or manual validation)
