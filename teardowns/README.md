# Daily Repo Teardown Log

A running archive of a daily habit: scan GitHub trending, keep the **3 most relevant repos plus 1 public knowledge vault**, and record why each one mattered.

## Why 3

Whatever the daily scan surfaces, only about one repo per day ever earns a real, focused exploration. Picking five candidates a day against a one-per-day follow-through rate just grows a backlog that never clears. Three keeps the funnel honest.

If fewer than three clear the bar on a given day, the entry records fewer. Padding to hit a number defeats the point.

## Format

Each day appends one block, newest first.

```markdown
### YYYY-MM-DD

| # | Repo | Stars today | What it is, why it is worth the time, the angle | Verdict |
|---|---|---|---|---|
| 1 |  |  |  |  |
| 2 |  |  |  |  |
| 3 |  |  |  |  |
| V | (public vault pick) | n/a |  |  |

**If you take one:**
**Notes:**
```

**Verdicts:** `teardown` (worth a full write-up) · `toolbox` (worth reusing in real work) · `vault-study` (structural patterns worth stealing) · `dropped`.

A block with no verdict means triage did not happen that day, which is itself worth seeing.

---

## Log

### 2026-07-23

| # | Repo | Stars today | What it is, why it is worth the time, the angle | Verdict |
|---|---|---|---|---|
| 1 | [`ComposioHQ/awesome-claude-skills`](https://github.com/ComposioHQ/awesome-claude-skills) (Python, 68.9k★) | +163 | A curated directory of Claude Skills, resources, and tools for customizing Claude workflows. Worth the time as a canonical public index of skills as a reusable unit rather than one-off prompts. **Angle:** sort the entries into those that add a capability versus those that encode a limit the agent cannot override, and see where the ratio falls. | |
| 2 | [`dottxt-ai/outlines`](https://github.com/dottxt-ai/outlines) (Python, 15.2k★) | +364 | Structured, constrained generation for LLMs: valid JSON, regex, and grammar-shaped output enforced at the decoding layer. Worth the time because it moves grounding from the prompt into the decoder. **Angle:** what that shift buys in reliability, and where a constrained decoder still cannot prevent a wrong answer. | |
| 3 | [`rohitg00/ai-engineering-from-scratch`](https://github.com/rohitg00/ai-engineering-from-scratch) (Python, 42.4k★) | +652 | A from-scratch AI-engineering reference and learning repository. Worth the time as a written-procedure artifact rather than a tool or framework. **Angle:** test where a from-scratch teaching order matches, or misses, what a single developer actually needs first. | |
| V | [`tirth8205/code-review-graph`](https://github.com/tirth8205/code-review-graph) | n/a | A local-first code intelligence graph exposed over MCP and CLI, built to reduce context for AI coding tools. Trending a third consecutive day, which earns it a closer look. **Angle:** what a local code graph gives an agent that raw file reads do not, and whether the context it saves justifies maintaining the graph. | |

**If you take one:** `ComposioHQ/awesome-claude-skills` — the most directly usable of the four, and a teardown that can be written without further research.
**Notes:** Star counts are as the trending page rendered them and were not verified against the GitHub API; no repo ages or creation dates were checked, so treat every number as a signal rather than a credential. *Notable but not picked:* `ayghri/i-have-adhd` (8.5k★, +1,699) and `diegosouzapw/OmniRoute` (25.6k★, +1,651) are both still climbing but were logged the previous day. `koala73/worldmonitor` (69.4k★, +4,139) is the fastest riser on the page but falls outside the scan's lanes with no clear teardown angle. Verdicts are empty by design: this block is written in the morning and triage runs later.

---

### 2026-07-22

| # | Repo | Stars today | What it is, why it is worth the time, the angle | Verdict |
|---|---|---|---|---|
| 1 | [`bojieli/ai-agent-book`](https://github.com/bojieli/ai-agent-book) (Python, 15.4k★) | +4,624 | An open repository of AI agent design principles and engineering practices, and the fastest riser on the page today. Worth the time because it is a written-procedure artifact rather than a tool or a framework, which is a comparatively rare shape in agent tooling. **Angle:** treat it as a canonical reference and test where its guidance holds up for single-developer setups rather than teams. | |
| 2 | [`ayghri/i-have-adhd`](https://github.com/ayghri/i-have-adhd) (7.1k★) | +1,866 | A coding-agent skill that reshapes output clarity and organization for neurodivergent users. Worth the time as a minimal example: one skill that changes output *format* rather than adding capability, and short enough to read end to end. **Angle:** what a presentation-only skill suggests about where the value in agent tooling actually sits. | |
| 3 | [`diegosouzapw/OmniRoute`](https://github.com/diegosouzapw/OmniRoute) (TypeScript, 23.8k★) | +2,034 | An AI gateway spanning 268+ providers and 500+ models with automatic fallback. Worth the time because provider routing is the infrastructure-level answer to inference cost and availability, not an application-level one. **Angle:** what routing buys in resilience versus what it costs in debuggability when a fallback fires silently. | |
| V | [`pbeens/obsidian-agents.md`](https://github.com/pbeens/obsidian-agents.md) | n/a | Agentic workflow configurations, instructions and skills built specifically for Obsidian note vaults, with Claude Code support. **Angle:** how a note-vault agent scopes its own permissions, and what it explicitly refuses to do. | |

**If you take one:** `ayghri/i-have-adhd`. It is the smallest of the four and the only one genuinely finishable in a single sitting.
**Notes:** Star counts are as the trending page rendered them and were not verified against the GitHub API; no repo ages or creation dates were checked, so treat every number as a signal rather than a credential. *Notable but not picked:* `tirth8205/code-review-graph` (24.7k★, +1,925) is trending a second consecutive day and the sustained velocity is worth noting. `KnockOutEZ/wigolo` (3.2k★, +642) is still climbing from an earlier scan. `1jehuang/jcode` and `agegr/pi-web` are both agent harnesses in a crowded category with no clear distinguishing angle. Verdicts are empty by design: this block is written in the morning and triage runs later.

---

### 2026-07-20

Log opened. First scan block lands on the next run.
