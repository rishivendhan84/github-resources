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

### 2026-07-25

| # | Repo | Stars today | What it is, why it is worth the time, the angle | Verdict |
|---|---|---|---|---|
| 1 | [`block/buzz`](https://github.com/block/buzz) (Rust, 10.4k★) | +3,270 | A self-hostable Nostr relay where humans and AI agents collaborate in shared channels on a single event log and keypair identity: agents join as team members, run workflows, and review code on the same audit trail as people. Worth the time as a shipped, infrastructure-level answer to the human-in-the-loop question of how a person and an agent share control of the same state. **Angle:** where a shared human-and-agent event log has to become an explicit approval boundary rather than a free-for-all, and what a single shared audit trail buys once an agent can act on the log unprompted. Fastest riser on the page today. | |
| 2 | [`shiyu-coder/Kronos`](https://github.com/shiyu-coder/Kronos) (Python, 33.6k★) | +499 | The first open-source foundation model for financial candlesticks (K-lines), trained on data from 45+ global exchanges: a specialized tokenizer converts OHLCV price data into discrete tokens, then an autoregressive Transformer forecasts. Worth the time as a rare concrete port of the LLM tokenizer-plus-Transformer recipe to noisy financial time-series rather than text. **Angle:** how it tokenizes continuous price data, since the tokenizer is the core bet, and what a forecasting model can and cannot responsibly promise before it informs a decision. | |
| 3 | [`OtterMind/Chat2DB`](https://github.com/OtterMind/Chat2DB) (Java, 26.4k★) | +82 | An AI-driven database client and SQL workspace: a full SQL editor plus an AI assistant that writes and optimizes queries across 30+ databases. Worth the time as a live example of an AI writing directly to real databases, which is a guardrail question more than a convenience one. **Angle:** what read-versus-write boundary it enforces before an AI-generated query touches production data, and whether query optimization is a safe place to hand control to a model. Lowest velocity of the three today (+82), included for topic fit rather than momentum. | |
| V | [`GuideThomas/obsidian-intelligence`](https://github.com/GuideThomas/obsidian-intelligence) | n/a | Makes an Obsidian note vault a first-class knowledge source for any MCP-enabled AI assistant: local, private, headless, with graph, full-text (FTS5), semantic, and hybrid (RRF) search, and notes never leaving the machine. **Angle:** how it scopes read-versus-write access to the vault and which search modality it reaches for first, a retrieval design worth studying for any local knowledge base exposed to an agent. Surfaced via search rather than the trending page, so unranked. | |

**If you take one:** `block/buzz` — the only one of the four that is directly write-up-ready rather than research-first, a working example of a shared human-and-agent workspace, and the fastest riser on the page today, so a teardown rides current attention.
**Notes:** Star counts are as the trending page rendered them and were not verified against the GitHub API; no repo ages or creation dates were checked, so treat every number as a signal rather than a credential. *Notable but not picked:* `koala73/worldmonitor` (73.6k★, +2,184) is the fastest riser on the page again but falls outside the scan's lanes with no clear teardown angle. `mattpocock/skills` (+2,251), `ComposioHQ/awesome-claude-skills` (+663), `diegosouzapw/OmniRoute` (+1,841), `likec4/likec4` (+337), `citrolabs/ego-lite` (+880), and `Automattic/harper` (+876) were all logged or noted on earlier days. Verdicts are empty by design: this block is written in the morning and triage runs later.

---

### 2026-07-24

| # | Repo | Stars today | What it is, why it is worth the time, the angle | Verdict |
|---|---|---|---|---|
| 1 | [`alibaba/open-code-review`](https://github.com/alibaba/open-code-review) (Go, 11.7k★) | +180 | An open-source code-review tool that runs deterministic pipelines with LLM-agent steps layered on top. Worth the time as a working example of splitting a review into fixed rule-based checks and model-judgment checks inside one pipeline. **Angle:** which checks it hard-codes as deterministic versus which it hands to the model, and what that dividing line says about where an LLM actually belongs in an automated pipeline. | |
| 2 | [`citrolabs/ego-lite`](https://github.com/citrolabs/ego-lite) (JavaScript, 1.8k★) | +247 | A web browser built so a person and an AI agent can work the same session in parallel. Worth the time as a concrete UI answer to the human-in-the-loop question: how a human and an agent share control of the same state. **Angle:** what parallel work really means when both touch the same state, and where the handoff has to become an explicit approval step rather than a silent merge. | |
| 3 | [`earthtojake/text-to-cad`](https://github.com/earthtojake/text-to-cad) (JavaScript, 10.1k★) | +230 | A collection of agent skills for CAD, robotics, and hardware design. Worth the time as a test of how far the idea of a reusable skill as the unit of work travels once it drives physical output instead of text. **Angle:** read one skill and see where a skill that drives hardware needs guarantees a text-only skill never does. | |
| V | [`likec4/likec4`](https://github.com/likec4/likec4) (TypeScript) | n/a | Architecture-as-code: describe a system in a small DSL and get live, navigable diagrams generated from the source. **Angle:** what it keeps in the model versus what it renders, and whether a live map generated from a single source of truth justifies maintaining the DSL over a hand-drawn diagram. | |

**If you take one:** `alibaba/open-code-review` — the most directly usable of the four, a working reference for splitting deterministic checks from model judgment in one pipeline.
**Notes:** Star counts are as the trending page rendered them and were not verified against the GitHub API; no repo ages or creation dates were checked, so treat every number as a signal rather than a credential. *Notable but not picked:* `ComposioHQ/awesome-claude-skills` (69.5k★, +636) and `diegosouzapw/OmniRoute` (27.5k★, +1,929) are both still climbing but were logged on earlier days. `koala73/worldmonitor` (71.9k★, +3,175) is the fastest riser on the page but falls outside the scan's lanes with no clear teardown angle. `Automattic/harper` (12.4k★, +624) is a local-first grammar checker, adjacent but thin as a teardown. Verdicts are empty by design: this block is written in the morning and triage runs later.

---

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
