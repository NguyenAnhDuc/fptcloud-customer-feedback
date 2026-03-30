# Database Rules

- MySQL 8.x via Flask-SQLAlchemy
- Use Flask-Migrate for all schema changes (never edit migrations manually — FROZEN)
- Table names: snake_case plural (e.g. `feedback_entries`)
- Always add `created_at`, `updated_at` timestamps
- UUID primary keys
- No raw SQL — use SQLAlchemy ORM
