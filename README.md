# Armand Al-Farizy

> What the human signs is exactly what the machine executes.

That sentence is the design rule behind most of what I build. AI agents are good at proposing actions and unreliable at deciding which ones are safe, so I put a human approval or a hard validation layer between the proposal and the effect, and I keep a record that can be checked afterwards.

## How that shows up in practice

| Principle | Where to see it |
| --- | --- |
| **The model proposes, the system decides.** A language model never has the last word on a destructive action. | [yomi-triage-system](https://github.com/ArcVielLouvent/yomi-triage-system) treats the model as an untrusted reasoner and gates containment with fixed rules. [kuro-sre-mcp](https://github.com/ArcVielLouvent/kuro-sre-mcp) runs a rollback only after an engineer approves it. |
| **Access is temporary by default.** Permission is granted for a scope and a time window, then expires without anyone remembering to revoke it. | [tegata](https://github.com/ArcVielLouvent/tegata) checks for a valid, unexpired grant on every request instead of trusting a status flag. |
| **Records should be verifiable, not just present.** | tegata keeps a hash-chained audit log and ships a script that recomputes the chain independently. Yomi seals each decision into a signed ledger. |
| **Agents connect outward.** Customer infrastructure should not need an open inbound port. | [StrataCore](https://stratacore.dev) uses an outbound-only agent. The protocol is documented with runnable code in [stratacore-agent-examples](https://github.com/ArcVielLouvent/stratacore-agent-examples). |

## Current work

**[StrataCore](https://stratacore.dev)** creates a preview environment for every pull request on servers the customer controls, and reports drift, spend and right-sizing across services. Built with Next.js, Supabase and Paddle, with billing changes that show the exact amount and require confirmation before anything is charged.

## Other projects

| Project | Summary |
| --- | --- |
| [tegata](https://github.com/ArcVielLouvent/tegata) | Time-boxed privileged access with a signed approval document, live enforcement and automatic expiry. Built for the DevNetwork API + Cloud + AI Hackathon 2026. |
| [yomi-triage-system](https://github.com/ArcVielLouvent/yomi-triage-system) | Incident response engine that drives SANS SIFT forensic tools through a type-safe MCP server. |
| [kuro-sre-mcp](https://github.com/ArcVielLouvent/kuro-sre-mcp) | MCP server that lets an AI assistant diagnose incidents from runbooks stored in Notion, with human approval before rollback. |
| [PJK-RM119-CareerMatch-AI](https://github.com/ArcVielLouvent/PJK-RM119-CareerMatch-AI) | Capstone project that matches CV skills to job postings with TF-IDF. |

## A lesson worth recording

Yomi was entered in the SANS Find Evil! hackathon and did not place. Its live containment design held up, but the competition rewarded depth of post-mortem analysis, and the project claimed more than it had tested. I rebuilt it with narrower claims and deeper test coverage; the plan and the per-phase log are in the repository. I would rather publish a smaller claim I can prove.

## Stack

TypeScript, Python, JavaScript, Next.js, Supabase, PostgreSQL, Model Context Protocol, GitHub Actions, Playwright, Cloudflare.

## Contact

The best way to reach me is a GitHub issue or discussion on the relevant repository.
