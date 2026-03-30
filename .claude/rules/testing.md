# Testing Rules

- pytest for backend (minimum: happy path + validation error per endpoint)
- Test file: `backend/tests/test_{module}.py`
- Use fixtures for DB setup/teardown
- No real DB in tests — use SQLite in-memory or mock
- Frontend: React Testing Library for components
