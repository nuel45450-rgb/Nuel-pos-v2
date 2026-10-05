# Nuel POS V2

## Stack
React + Vite / Node.js + Express / PostgreSQL

## Requirements
Node.js 20+ and PostgreSQL 15+.

## Setup
1. Create a database called `nuelpos`.
2. Run `server/schema.sql` against it.
3. Copy `server/.env.example` to `server/.env` and set DATABASE_URL and JWT_SECRET.
4. In `server`: `npm install` then `npm run dev`.
5. In `client`: `npm install` then `npm run dev`.
6. Open the Vite URL, normally http://localhost:5173.
7. If there is no user, create the first owner with POST `/api/setup/owner`; easiest with PowerShell/curl:
   `curl -X POST http://localhost:4000/api/setup/owner -H "Content-Type: application/json" -d "{\"name\":\"Owner\",\"username\":\"owner\",\"password\":\"1234\"}"`
8. Log in and change the starter password before real use.

Features: dashboard, products, direct sales with no cart, sales history, expenses, reports, stock movement, users, activity log, secure password hashing, role permissions, PostgreSQL persistence, and End Day summaries.
