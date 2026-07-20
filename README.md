# GitHub Project Notes

A working archive of project ideas and daily repo teardowns.

## Contents

| File | What it is |
|---|---|
| [github-resources.md](github-resources.md) | The standing GitHub resource index by domain, seeded with 170 entries across 16 domains, each with a repo or topic link |
| [teardowns/](teardowns/) | The daily repo teardown log: 3 trending repos + 1 public vault per day, with a verdict on each |

## How the daily scan works

Every morning the scan pulls `github.com/trending?since=daily` plus a rising-repo search, filters to a working set of lanes (AI agents, MCP, LLM tooling, automation, frontend and AI), and keeps the **top 3 repos plus 1 public knowledge vault**.

Each pick is one line: what it is, why it is worth the time, and the teardown or tooling angle. Everything then gets a 10-minute triage and one of four verdicts:

- `teardown` : worth a full write-up
- `toolbox` : worth reusing in real work
- `vault-study` : structural patterns worth stealing
- `dropped` : no further action

At most one repo per day is promoted to a real timeboxed exploration. That cap is why the daily count is 3 and not 5: five candidates a day against a one-per-day promotion rate only ever grows the queue.

## The teardown trick

Swap `github.com` for `gitingest.com` in any repo URL to get the whole repo as a single text blob, then feed it to an LLM for a first-pass teardown draft. That one substitution is what makes a daily cadence sustainable.

## Status

Actively maintained. The list grows as new batches are added; the teardown log appends daily.
