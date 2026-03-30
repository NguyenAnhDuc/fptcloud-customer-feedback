# AGENTS.md — fptcloud-customer-feedback

> Single source of truth. CLAUDE.md symlinks here.
> `ln -s AGENTS.md CLAUDE.md`

Customer Feedback Widget for FPT Cloud Console — AI-Centered Engineering POC (O2 Q2/2026).
Stack: React + MUI (frontend) · Python Flask 3.x (backend) · MySQL · REST /api/v1/ · FPT ID OAuth

## Commands
- `cd backend && flask run` — run backend dev server
- `cd frontend && npm start` — run frontend dev server
- `cd backend && pytest` — run tests
- `cd backend && flake8 app/` — lint backend
- `cd backend && black app/` — format backend

## Zone map
FROZEN (hotfix only — AI MUST NOT touch without explicit instruction):
- `backend/app/auth/` — FPT ID OAuth integration
- `backend/migrations/` — do not modify existing migrations

GROWTH (new features OK):
- `backend/app/api/v1/feedback/`
- `frontend/src/components/FeedbackWidget/`
- `frontend/src/pages/AdminReport/`

## Gold standard
No gold module yet — use CONSTITUTION.md as reference for API patterns.

## Cross-repo
API contract frozen in CONSTITUTION.md — both FE and BE must follow.

## Skill Activation
| Task | Skill |
|------|-------|
| Review code | .claude/skills/code-review/SKILL.md |
