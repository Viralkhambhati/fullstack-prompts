# 50 Proven Prompts to Build a Full-Stack Web Application

Frontend -> Backend -> Database (plus Auth, Testing, and Deployment)

## How to use this doc (fast):

1. Pick a stack (example: React + Node/Express + PostgreSQL).
2. Copy the prompts in order. Paste into your AI assistant (ChatGPT / Copilot / Claude / etc.).
3. Replace placeholders like `{APP_NAME}`, `{FEATURES}`, `{DB_NAME}`.
4. After each prompt, run the code, confirm it works, then move to the next prompt.

## Project Spec Template (paste once before Prompt #1):

```text
APP_NAME: {APP_NAME}
GOAL: {1 sentence goal}
USERS: {user types}
CORE FEATURES: {feature list}
STACK: {frontend}, {backend}, {database}
AUTH: {email/password | OAuth | none}
DEPLOY TARGET: {Vercel/Netlify + Render/Fly/Azure/etc.}
NON-FUNCTIONAL: {performance, security, logging, monitoring}
STYLE: Clean UI, mobile-first, accessible, simple.
```

## The 50 Prompts (copy-paste)

Tip: paste prompts one by one. After each prompt, run the code, commit, and move to the next prompt.
Each prompt is inside a code block so GitHub shows a copy button.

<details>
<summary>Prompt #1: Define scope & MVP</summary>

```text
Act as a senior product engineer. Based on the Project Spec, produce:
- MVP scope (must-have vs nice-to-have)
- Key user flows (happy path + edge cases)
- Data objects (entities) and relationships
Keep it short and actionable.
```
</details>

<details>
<summary>Prompt #2: System architecture map</summary>

```text
Create an architecture plan for this full-stack app:
- Frontend pages/components
- Backend modules/routes
- Database tables + indexes
- Auth approach
- Error handling and logging
Return as a bullet list + a simple diagram in text.
```
</details>

<details>
<summary>Prompt #3: API contract first</summary>

```text
Design the API contract (REST):
- Endpoints, methods, request/response JSON
- Validation rules
- Error shapes (standard format)
- Pagination and filtering if needed
Return a concise OpenAPI-style outline.
```
</details>

<details>
<summary>Prompt #4: DB schema draft</summary>

```text
Design the database schema:
- Table definitions (columns, types, constraints)
- Relationships and cascade rules
- Indexes that matter
- Seed data plan
Return SQL (PostgreSQL).
```
</details>

<details>
<summary>Prompt #5: Folder structure</summary>

```text
Propose a repository structure (monorepo or separate):
- frontend/
- backend/
- shared/ (types)
Include scripts for dev, test, and build.
```
</details>

<details>
<summary>Prompt #6: Local dev checklist</summary>

```text
Write a step-by-step local setup checklist (fresh machine):
- prerequisites
- env vars
- run DB
- run backend
- run frontend
Also include common fixes when ports or env vars break.
```
</details>

<details>
<summary>Prompt #7: Frontend bootstrap</summary>

```text
Generate the frontend starter (React + Vite + TypeScript):
- routing
- global layout
- API client wrapper (fetch/axios)
- environment config
Return exact commands + file contents.
```
</details>

<details>
<summary>Prompt #8: Design system basics</summary>

```text
Create a minimal UI system:
- spacing scale
- typography scale
- button/input/card styles
- reusable components (Button, Input, Modal, Toast)
Ensure accessibility (labels, focus).
```
</details>

<details>
<summary>Prompt #9: Page list & wireframes</summary>

```text
List the pages required for the MVP and provide quick wireframes in text:
- header/footer/nav
- empty/loading/error states per page.
```
</details>

<details>
<summary>Prompt #10: State management plan</summary>

```text
Recommend state handling (React Query + context, or similar):
- what goes in server state vs UI state
- caching rules
- loading/error UX patterns.
```
</details>

<details>
<summary>Prompt #11: Auth screens</summary>

```text
Generate UI screens for auth:
- sign up
- sign in
- forgot password (if used)
Include form validation and inline error messages.
```
</details>

<details>
<summary>Prompt #12: Dashboard / main screen UI</summary>

```text
Generate the main dashboard UI for the core flow:
- data table or cards
- filters/search
- create/edit dialogs
Include responsive behavior.
```
</details>

<details>
<summary>Prompt #13: Detail view + edit flow</summary>

```text
Add a detail page with edit mode:
- view state
- edit state with validation
- save/cancel UX
Use optimistic updates if appropriate.
```
</details>

<details>
<summary>Prompt #14: Reusable form builder</summary>

```text
Create a reusable form helper:
- schema validation (Zod/Yup)
- reusable FormField component
- consistent error display
Show example usage on one form.
```
</details>

<details>
<summary>Prompt #15: Client-side routing guards</summary>

```text
Add protected routes:
- redirect unauthenticated users to login
- preserve intended destination
- handle token expiry gracefully.
```
</details>

<details>
<summary>Prompt #16: Frontend error boundaries</summary>

```text
Add an ErrorBoundary and a consistent error page:
- user-friendly messaging
- retry button
- log details in dev only.
```
</details>

<details>
<summary>Prompt #17: Frontend testing plan</summary>

```text
Write a testing plan for frontend:
- unit tests for components
- integration tests for main flows
- recommended tools + sample test.
```
</details>

<details>
<summary>Prompt #18: Performance basics</summary>

```text
Improve frontend performance:
- code splitting
- image optimization
- avoid re-renders
Provide concrete code changes.
```
</details>

<details>
<summary>Prompt #19: Backend bootstrap</summary>

```text
Generate backend starter (Node.js + Express + TypeScript):
- linting, formatting
- env handling
- health endpoint
- structured logging
Return commands + file tree + key files.
```
</details>

<details>
<summary>Prompt #20: DB connection layer</summary>

```text
Implement DB layer (Prisma/Knex/pg):
- connection setup
- migrations
- repository pattern
Include sample query functions.
```
</details>

<details>
<summary>Prompt #21: Auth implementation</summary>

```text
Implement auth for the chosen approach:
- password hashing + salting (if email/password)
- JWT/session handling
- refresh strategy (if used)
- secure cookies (if web)
Include middleware + example routes.
```
</details>

<details>
<summary>Prompt #22: User model + validation</summary>

```text
Create user entity:
- create user
- login
- get current user (/me)
Add validation + consistent error responses.
```
</details>

<details>
<summary>Prompt #23: CRUD: create</summary>

```text
Implement the Create endpoint for the main entity:
- validation
- authorization rules
- DB write
- return JSON that matches the API contract.
```
</details>

<details>
<summary>Prompt #24: CRUD: read list</summary>

```text
Implement List endpoint:
- pagination
- filtering/search
- sorting
- return total count
Include SQL/index notes.
```
</details>

<details>
<summary>Prompt #25: CRUD: read single</summary>

```text
Implement Get-by-id endpoint:
- 404 handling
- authorization
- include related data if needed.
```
</details>

<details>
<summary>Prompt #26: CRUD: update</summary>

```text
Implement Update endpoint:
- partial update (PATCH) vs full update (PUT)
- validation rules
- concurrency strategy (updated_at or version)
```
</details>

<details>
<summary>Prompt #27: CRUD: delete</summary>

```text
Implement Delete endpoint:
- soft delete vs hard delete
- audit fields
- authorization
Return response standard.
```
</details>

<details>
<summary>Prompt #28: Rate limiting + security headers</summary>

```text
Add basic protection:
- rate limiting on auth routes
- security headers (helmet)
- CORS config for the frontend origin
Explain the settings.
```
</details>

<details>
<summary>Prompt #29: Central error handler</summary>

```text
Implement a global error handler:
- map known errors to status codes
- preserve stack traces in dev only
- unify error JSON shape.
```
</details>

<details>
<summary>Prompt #30: Request logging + tracing</summary>

```text
Add request logging:
- request id
- timing
- user id (if available)
Show example log line format.
```
</details>

<details>
<summary>Prompt #31: Backend tests</summary>

```text
Create backend tests:
- unit tests for services
- integration tests for routes using a test DB
Provide at least 2 sample tests.
```
</details>

<details>
<summary>Prompt #32: API docs</summary>

```text
Generate API documentation:
- OpenAPI spec file
- how to render Swagger UI
- examples for each endpoint.
```
</details>

<details>
<summary>Prompt #33: Background jobs (optional)</summary>

```text
If this app needs async work (emails, processing):
- propose a job queue
- implement one sample job + worker
If not needed, say 'skip' and why.
```
</details>

<details>
<summary>Prompt #34: File uploads (optional)</summary>

```text
If the app needs uploads:
- choose storage (S3/Azure Blob/local for dev)
- implement signed upload flow
- validate type/size
If not needed, say 'skip'.
```
</details>

<details>
<summary>Prompt #35: Migrations workflow</summary>

```text
Set up migrations:
- create migration
- apply migration
- rollback strategy
Include scripts and best practices.
```
</details>

<details>
<summary>Prompt #36: Seed data</summary>

```text
Create seed scripts for local/dev:
- sample users
- sample entities
- deterministic data
Include how to run it.
```
</details>

<details>
<summary>Prompt #37: Indexes & query tuning</summary>

```text
Review the schema and propose indexes:
- explain why each index helps
- show the SQL
Also mention common slow queries to watch.
```
</details>

<details>
<summary>Prompt #38: Data validation at DB level</summary>

```text
Add DB constraints:
- unique constraints
- foreign keys
- check constraints
Explain how they prevent bugs.
```
</details>

<details>
<summary>Prompt #39: Audit fields</summary>

```text
Add audit columns:
- created_at, updated_at, deleted_at (if soft delete)
- created_by, updated_by (if needed)
Update code to write these fields.
```
</details>

<details>
<summary>Prompt #40: Transactions</summary>

```text
Find one risky multi-step operation and wrap it in a transaction:
- show the code
- show rollback behavior on failure.
```
</details>

<details>
<summary>Prompt #41: Backups & restore plan</summary>

```text
Create a simple backup/restore plan:
- dev
- staging
- production
Include retention + how to test restores.
```
</details>

<details>
<summary>Prompt #42: Observability hooks</summary>

```text
Add basic observability:
- metrics endpoint (or logs-based metrics)
- structured logs for key actions
- health checks (liveness/readiness)
```
</details>

<details>
<summary>Prompt #43: Security review checklist</summary>

```text
Review security:
- auth/session handling
- input validation
- injection risks
- secrets management
Return a checklist + quick fixes.
```
</details>

<details>
<summary>Prompt #44: Smoke test script</summary>

```text
Write a smoke test script that hits:
- /health
- auth flow (if used)
- one create/read/update path
Return a runnable script (bash or node).
```
</details>

<details>
<summary>Prompt #45: Containerize backend</summary>

```text
Create a Dockerfile for backend:
- small image
- non-root user
- env var usage
- healthcheck
Also write a docker-compose for local full stack.
```
</details>

<details>
<summary>Prompt #46: Deploy plan</summary>

```text
Create a deploy plan for:
- frontend hosting
- backend hosting
- database hosting
Include env vars, secrets, and domain/HTTPS steps.
```
</details>

<details>
<summary>Prompt #47: CI pipeline</summary>

```text
Create a CI pipeline that runs:
- lint
- tests
- build
- security checks (basic)
Return a GitHub Actions YAML (or Azure DevOps YAML if I request).
```
</details>

<details>
<summary>Prompt #48: Release checklist</summary>

```text
Write a release checklist:
- migrations
- config checks
- monitoring/alerts
- rollback steps
Make it short and realistic.
```
</details>

<details>
<summary>Prompt #49: Prompt to iterate features safely</summary>

```text
When I ask for a new feature, follow this workflow:
1) restate requirements + edge cases
2) propose minimal code changes
3) update API + DB if needed
4) update frontend
5) add tests
6) show how to verify locally
Return as a reusable instruction prompt.
```
</details>

<details>
<summary>Prompt #50: Prompt to debug production issues</summary>

```text
When I report a bug, ask for:
- exact error message/logs
- steps to reproduce
- env details
Then propose:
- most likely root causes
- step-by-step investigation
- safest fix + verification
Return as a reusable instruction prompt.
```
</details>

## One-pass Build Flow (suggested order)

1. Prompts 1-6: scope, architecture, API contract, schema, repo layout
2. Prompts 7-18: frontend foundation and UI flows
3. Prompts 19-34: backend + APIs + auth + tests
4. Prompts 35-44: DB reliability, observability, security
5. Prompts 45-50: containerize, deploy, CI, iterate

## CTA (optional):

Want the full prompt pack? Comment "PROMPTS" and I'll share it.
