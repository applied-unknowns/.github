# Governance

How decisions are made in Applied Unknowns. This is stage one: a single approver, written rules, and permissions that grow only with demonstrated reliability.

## Who decides

Justin Hilliard is the founder and the sole approver. Anyone, human or agent, may propose. Nothing changes without his approval, recorded as a merged pull request.

## How rules change

Rules live in [`AGENTS.md`](AGENTS.md). Each carries a status: **Set** (Justin stated it, in force) or **Proposed** (an agent drafted it, not in force). A rule changes through a pull request that names the rule and the reason. Rules are amended, never replaced wholesale.

## Permission ladder

| What agents may do | Status |
| --- | --- |
| On their own: triage issues, investigate failing checks, write documentation, suggest refactors | Allowed, through pull requests and issues |
| Only with Justin's approval: merge, deploy, change security settings | Justin approves each one |

Moving any kind of work from the second row to the first requires written promotion criteria, built from evidence over time. None exist yet.

## Records

- Decisions: merged pull requests, and architecture decision records (ADRs) once they exist
- Lessons and exceptions: [`foundation/LESSONS.md`](https://github.com/applied-unknowns/foundation/blob/main/LESSONS.md)
- Waiting on a decision: [`foundation/OPEN.md`](https://github.com/applied-unknowns/foundation/blob/main/OPEN.md)
- Planned work: [`foundation/BACKLOG.md`](https://github.com/applied-unknowns/foundation/blob/main/BACKLOG.md)
- Repository registry: [`foundation/INDEX.md`](https://github.com/applied-unknowns/foundation/blob/main/INDEX.md)
