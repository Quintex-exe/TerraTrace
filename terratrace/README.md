# TerraTrace OSINT

Lawful, evidence-based photo geolocation analysis. Early foundation only.
No upload, auth, mapping, or admin features yet.

## Layout

```
backend/    FastAPI API (Python 3.12)
frontend/   React + TypeScript + Vite
storage/    Local uploads (git-ignored)
docs/       Documentation
```

## Requirements

- Python 3.12
- Node.js 20+

## Setup

```bash
cp .env.example .env
```

### Backend

```bash
cd backend
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements-dev.txt
uvicorn app.main:app --reload
```

Health check: http://127.0.0.1:8000/api/health

Tests:

```bash
cd backend && pytest
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

Open http://localhost:5173

## Security

Never commit `.env`. Use placeholder values in `.env.example` only.
