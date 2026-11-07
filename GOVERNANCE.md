# Governance

How decisions are made in Applied Unknowns. This is organization policy, read by reference; GitHub does not apply this file to other repositories automatically. This is stage one: a single approver, written rules, and permissions that grow only with demonstrated reliability.

## Who decides

Justin Hilliard is the founder and the sole approver of organization policy. Anyone, human or agent, may propose. Justin's approval is required for changes outside the Stage B exception in rule 2 and is recorded as a merged pull request. Only for eligible Stage B pull requests in `applied-unknowns/wolfkrow-v2` may an independent model review satisfy the technical approval requirement under rule 2.

## How rules change

Rules live in [`AGENTS.md`](https://github.com/applied-unknowns/.github/blob/main/AGENTS.md). Each carries a status: **Set** (Justin stated it, in force) or **Proposed** (an agent drafted it, not in force). A rule changes through a pull request that names the rule and the reason. Rules are amended, never replaced wholesale.

## Permission ladder

| Work | Who does it |
| --- | --- |
| Triage issues, investigate failing checks, write documentation, suggest refactors | Agents, on their own, through pull requests and issues |
| Deploy, change security settings | Agents only with Justin's explicit approval for each one |
| Merge | Justin by default. The sole exception is an ordinary, eligible `applied-unknowns/wolfkrow-v2` Stage B pull request automatically merged under the exact conditions in Set rule 2, including any applicable founder code-owner approval for protected paths. Stage 1a dispatcher pilot pull requests remain founder-merged. No other repository inherits this exception. |

Moving any kind of work from the second row to the first requires written promotion criteria, built from evidence over time. None exist yet. Justin granted the `applied-unknowns/wolfkrow-v2` Stage B merge exception ahead of written promotion criteria in his [2026-11-07 GC-1 decision](https://github.com/applied-unknowns/wolfkrow-v2/issues/93#issuecomment-6702523258), choosing Option A to adopt the amendment and then run the six negative tests.

## Records

- Decisions: merged pull requests, and architecture decision records (ADRs) once they exist
- Lessons and exceptions: [`foundation/LESSONS.md`](https://github.com/applied-unknowns/foundation/blob/main/LESSONS.md)
- Waiting on a decision: [`foundation/OPEN.md`](https://github.com/applied-unknowns/foundation/blob/main/OPEN.md)
- Planned work: [`foundation/BACKLOG.md`](https://github.com/applied-unknowns/foundation/blob/main/BACKLOG.md)
- Repository registry: [`foundation/INDEX.md`](https://github.com/applied-unknowns/foundation/blob/main/INDEX.md)
