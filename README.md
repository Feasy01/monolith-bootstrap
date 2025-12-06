# Monolith Bootstrap

A lightweight monorepo starter with a React front-end and FastAPI back-end.

## Frontend (React + Vite + Tailwind + shadcn + React Query)

```
cd frontend
npm install
npm run dev
```

- Component structure under `src/components`, `src/containers`, `src/pages`, and `src/utils`.
- TailwindCSS configured via `tailwind.config.cjs` and `postcss.config.js`.
- React Query wired up to the FastAPI health endpoint.

## Backend (FastAPI)

```
cd backend
uv venv
source .venv/bin/activate
uv sync
uvicorn app.main:app --reload
```

- Routes live in `app/routes`, services in `app/services`, and database feature modules under `app/database`.
- Includes a lifespan hook using FastAPI's `lifespan` context and a health endpoint at `/health`.

## Project layout

```
frontend/  # React client
backend/   # FastAPI server
```

Start both servers to see the landing page report the API health.
