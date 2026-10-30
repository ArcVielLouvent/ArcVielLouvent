# Armand Al-Farizy

I build security and platform-engineering tools in which AI agents propose actions and a human, or a hard validation layer, decides what actually runs. My recent work focuses on access control, incident response and developer infrastructure.

## Current work

**[StrataCore](https://stratacore.dev)** is a SaaS platform that creates a preview environment for every pull request on servers the customer controls, and reports drift, spend and right-sizing across services. It is built with Next.js, Supabase and Paddle. A reference for connecting your own infrastructure to it is public: [stratacore-agent-examples](https://github.com/ArcVielLouvent/stratacore-agent-examples).

## Selected projects

| Project | Summary | Stack |
| --- | --- | --- |
| [tegata](https://github.com/ArcVielLouvent/tegata) | Time-boxed privileged access. An AI drafts the request, a human signs a real document, access is enforced on every request and expires automatically. Includes a hash-chained audit log that can be verified independently. | TypeScript, Python |
| [yomi-triage-system](https://github.com/ArcVielLouvent/yomi-triage-system) | Digital forensics and incident response engine that drives SANS SIFT tools through a type-safe MCP server. The language model is treated as untrusted; destructive actions are gated by fixed rules and recorded in a signed ledger. | Python |
| [kuro-sre-mcp](https://github.com/ArcVielLouvent/kuro-sre-mcp) | MCP server that lets an AI assistant diagnose incidents from runbooks held in Notion. A rollback runs only after an engineer approves it. | JavaScript |
| [PJK-RM119-CareerMatch-AI](https://github.com/ArcVielLouvent/PJK-RM119-CareerMatch-AI) | Capstone project that matches CV skills to job postings using TF-IDF. | Python, Jupyter |

## Areas of focus

- Human-in-the-loop design for AI agents, including approval gates and tamper-evident audit trails
- Access control, secrets handling and multi-tenant isolation
- Developer infrastructure: preview environments, CI pipelines, cost and drift visibility
- Applied machine learning and MLOps workflows

## Tools

TypeScript, Python, JavaScript, Next.js, Supabase, PostgreSQL, Model Context Protocol, GitHub Actions, Playwright, Cloudflare.

## Contact

The best way to reach me is through a GitHub issue or discussion on the relevant repository.
