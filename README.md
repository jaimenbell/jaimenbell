### Reliability engineering for AI-agent systems

I find and fix the failure that takes agent-run software down: an automation with more
access than the job needs, a destructive command with no gate in front of it, or a job
that reports "done" without checking what it touched.

**What I build**

- **[mcp-security-scanner](https://github.com/jaimenbell/mcp-security-scanner)** — static scanner for MCP / agent servers. 7 detector families
  (codegen injection, tool-param injection, auth posture, secret handling, tool-scope creep,
  secret-leak-via-response, destructive job-file hazards). Every finding: severity · file:line
  · fix · honest confidence. Dogfooded via a self-audit across an 8-server fleet.
- **Production MCP servers** — auth-scoped tool groups, write access off by default, honest
  capability tables, real test suites. Several are public here 👇

**Public reference servers**

| Repo | What it is |
|---|---|
| [mcp-security-scanner](https://github.com/jaimenbell/mcp-security-scanner) | Static security scanner for MCP/agent servers |
| [mcp-factory](https://github.com/jaimenbell/mcp-factory) | MCP scaffold + runtime hub |
| [github-mcp](https://github.com/jaimenbell/github-mcp) | Read+write GitHub REST MCP server, write group env-gated off |
| [desktop-mcp](https://github.com/jaimenbell/desktop-mcp) | Windows desktop control, input group off by default |
| [bus-mcp](https://github.com/jaimenbell/bus-mcp) | Multi-agent coordination bus, write-gated |
| [rails-mcp](https://github.com/jaimenbell/rails-mcp) | Governance rails: action registry + irreversibility gates |
| [vllm-ops-mcp](https://github.com/jaimenbell/vllm-ops-mcp) | Local-inference ops server (vLLM) |

I run a productized reliability + MCP practice at **[jaimenbell.dev](https://jaimenbell.dev)**.
No fabricated metrics, no client logos — public, testable code is the proof.

📫 jaime@jaimenbell.dev
