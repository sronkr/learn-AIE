# learn-AIE

Hands-on AI engineering. Building LLM-powered systems from the API layer up,
then using them in three projects.

Four weeks of fundamentals, then eight weeks of project work. Each week has a
build exercise and a check that has to pass before the next one starts. Notes
record what broke and why.

## Contents

| Folder | Topic |
| --- | --- |
| `week-00/` | Environment, streaming, Postgres, CI |
| `week-01/` | Provider APIs, structured outputs, caching, cost and latency |
| `week-02/` | Embeddings, chunking, hybrid retrieval, grounded answers |
| `week-03/` | Tool use, agent loops, durable state, MCP, agent security |
| `week-04/` | Evaluation, tracing, deployment, fine-tuning |
| `projects/` | Three end-to-end builds |
| `packages/` | Shared code extracted from the projects |

## Setup

```bash
git clone https://github.com/sronkr/learn-AIE.git
cd learn-AIE
cp .env.example .env   # fill in your own keys
```

Requires git, [uv](https://docs.astral.sh/uv/), Node 22, and Docker Desktop.

## Stack

Python with FastAPI and Pydantic, TypeScript with Next.js and Zod, Postgres with
`pgvector`, Redis, Docker Compose. Model access through a provider adapter so the
backend is not tied to one vendor.
