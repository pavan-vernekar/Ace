# Decision Log

A running log of architecture and product decisions made while building Forks.

## 2026-XX-XX — Free-tier-only constraint
**Context:** Building Forks as a portfolio + open-source project, no infra budget.
**Decision:** All services free-tier only — Vercel, Supabase, Gemini, Groq, Resend.
**Tradeoffs accepted:** Rate limits, prompts may be used for training, no SLAs.
**Rationale:** Constraint becomes a marketing asset. "$0/month production agent" is the launch hook.

## 2026-XX-XX — Gemini-primary over local-first
**Context:** Choosing the primary LLM provider.
**Decision:** Gemini 2.5 Pro primary, Groq Llama 3.3 70B for extraction, Ollama deferred to v1.1.
**Tradeoffs accepted:** Cloud dependency, privacy disclosure required.
**Rationale:** Demo speed and reliability matter most for a 14-day launch. Ollama mode in v1.1 = second content wave.