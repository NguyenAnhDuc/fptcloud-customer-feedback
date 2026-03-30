# Project Structure

```
fptcloud-customer-feedback/
├── AGENTS.md                    ← Single source of truth
├── CLAUDE.md                    → symlink to AGENTS.md
├── CONSTITUTION.md              ← API contract (frozen after Day 3)
├── .claude/
│   ├── settings.json            ← Hooks (100% enforcement)
│   ├── rules/                   ← Auto-load conventions
│   ├── skills/
│   │   └── code-review/
│   └── agents/
├── backend/
│   ├── app/
│   │   ├── __init__.py          ← Flask app factory
│   │   ├── auth/                ← FROZEN: FPT ID OAuth
│   │   ├── api/v1/feedback/     ← GROWTH: main feature
│   │   └── models/
│   ├── migrations/              ← FROZEN: use flask db migrate
│   ├── tests/
│   └── requirements.txt
└── frontend/
    ├── src/
    │   ├── components/FeedbackWidget/
    │   └── pages/AdminReport/
    └── package.json
```
