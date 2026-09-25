# learn-AIE

Hands-on AI engineering workspace. Four weeks of fundamentals, then three
end-to-end projects built on top of them.

## Layout

- `week-XX/` — one folder per week: notes, the build exercise, a README on what broke
- `projects/` — the three end-to-end projects
- `packages/` — shared code extracted from the projects (provider adapter, eval runner, tracing)

## Conventions

- Python: `uv` for environments, Pydantic v2 for all model I/O, `pytest` for tests
- TypeScript: strict mode, Zod for schemas, `vitest` for tests
- Postgres + Redis via Docker Compose; `pgvector` for embeddings
- Use `pathlib` in Python and `path.join` in Node. Never hardcode path separators:
  this repo is edited on Windows and macOS and deploys to Linux.
- Every week ends with a check. Do not start the next week until it passes.

## Working rules

- Hand-write the core loop of each week once (API call, retriever, agent loop, eval
  runner) before reaching for a framework. The point is to be able to explain it.
- Treat models as untrusted. Validate every structured output, sandbox every tool.
- Secrets live in `.env`, which is ignored. `.env.example` lists the required keys.

## Hygiene

This repository is public.

- Never commit keys or connection strings.
- Never commit real user data. One project involves a real user: anonymize first.
- Check `git status` before `git add -A`.

## Cross-machine notes

- This repo is the sync mechanism between the Windows desktop and the MacBook Air.
- Session history and auto-memory do not sync. Push before switching machines.
- `.claude/settings.local.json` and `CLAUDE.local.md` are per-machine and ignored.
