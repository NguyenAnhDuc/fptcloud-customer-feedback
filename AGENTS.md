# AGENTS.md — fptcloud-customer-feedback

> Single source of truth. CLAUDE.md symlinks here.
> `ln -s AGENTS.md CLAUDE.md`

New feature module for FPT Cloud Console — Vietnam's public cloud platform (IaaS/PaaS, comparable to AWS/GCP).
This repo adds a Customer Feedback Widget to the existing console (console.fptcloud.com) as part of O2 Console Experience Q2/2026.
The console is a React+MUI SPA. This module adds: (1) an in-console feedback widget for end users, (2) an admin report page for internal teams.
Stack: React + MUI (frontend, integrates into existing console) · Python Flask 3.x (new microservice) · MySQL · REST /api/v1/ · FPT ID OAuth (existing auth, reuse tokens)

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
