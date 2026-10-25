# Rules for agents in Applied Unknowns

Read this file before reading or changing anything in this organization. It is the one instruction layer for every agent, whatever model or vendor runs it. Then, once they exist, read [`OPEN.md`](https://github.com/applied-unknowns/foundation/blob/main/OPEN.md) and [`LESSONS.md`](https://github.com/applied-unknowns/foundation/blob/main/LESSONS.md) in the `foundation` repository. Both are pending as of 2026-10-25.

Applied Unknowns is Justin Hilliard's company and the first formation of a larger research collective. This organization is its public, governed home. Agents work here as collaborators, under rules that are written down, versioned, and changed only through review.

Every rule carries a status. **Set** means Justin stated it and it is in force. **Proposed** means an agent drafted it and it is not in force until Justin accepts it. Only Justin moves a rule from Proposed to Set.

## Identities

| Account | Who it is | Used for | Branch prefix | Commit email |
| --- | --- | --- | --- | --- |
| `jhilliardx` | Justin. Organization owner and sole approver. | Approving, merging, settings. Never used by an agent for agent work. | `jhilliardx/` | `151980015+jhilliardx@users.noreply.github.com` |
| `jhilliardx-claude-ai` | Claude (Anthropic), member of the `agents` team | Authoring branches, pull requests, reviews, issues | `claude/` | `347296035+jhilliardx-claude-ai@users.noreply.github.com` |
| `jhilliardx-chatgpt-ai` | ChatGPT (OpenAI), member of the `agents` team | Authoring branches, pull requests, reviews, issues | `chatgpt/` | `347296528+jhilliardx-chatgpt-ai@users.noreply.github.com` |

These are interim user accounts. They will be replaced by one GitHub App per vendor once agents run through application programming interface (API) access.

## Rules

| # | Rule | Status |
| --- | --- | --- |
| 1 | Anyone, human or agent, may propose. Justin is the sole approver. | Set |
| 2 | Agents change any repository through a branch and a pull request. Justin merges. No agent merges, and no agent holds a ruleset bypass. | Set |
| 3 | Before any write, an agent names the identity it is writing as. An agent writes only as its own account. | Set |
| 4 | The record says who did what. When one party carries another's work (for example, Justin uploading files an agent drafted), the commit or pull request states the author. | Set |
| 5 | Review is independent: the reviewer of a pull request is never its author. | Set |
| 6 | Elicitation is independent; review shares an input. Models form their first view without seeing each other's, then review the same artifact. | Set |
| 7 | Rules are amended, never replaced. A change to this file is a pull request that names the rule it changes and why. | Set |
| 8 | Everything is public unless/until something needs to be private. No credentials, private personal information, or other confidential material enter any repository. | Set |
| 9 | Three things never enter this organization: Justin's personal and family matters (personal projects may be brought in; his personal life may not), anything with a nexus to his employer, and anything that violates the organization's values. | Set |
| 10 | Open items and decisions waiting on Justin are written to a persistent list, never left only in a conversation. | Set |
| 11 | Before building, the author plays back the target and assumptions in a few lines. When something misses, correct the target instead of patching the output. | Set |
| 12 | Writing is plain and literal. Spell out each acronym at first use. Avoid em dashes. Agent conclusions are labeled as agent conclusions; statements attributed to Justin are things he said. | Set |
| 13 | Changes to `AGENTS.md`, `CODEOWNERS`, the pull request template, and workflow files require Justin's review as code owner. | Set |
| 14 | A branch is named `<prefix>/<short-purpose>`, where the prefix belongs to the account that pushes it (see Identities). | Proposed |
| 15 | Co-author credit uses the account's commit email from the Identities table, never a vendor's generic address. A generic vendor address credits the vendor's own GitHub account, which is outside this organization. | Proposed |
| 16 | A pull request merged without an independent review states why in the pull request, and the exception is logged in `foundation/LESSONS.md`. | Proposed |

The pull request ruleset is active. As organization admin, Justin can merge a pull request without its required approvals; he cannot push directly to main. Agents have no bypass. Required code-owner approvals are not yet enabled; rule 13 states the review policy and `CODEOWNERS` prepares for platform enforcement.

## Authoring a pull request

1. Name your identity in the first line of the pull request body.
2. Fill in the pull request template completely. Choose exactly one review shape and write the one question you most want answered.
3. Keep one purpose per pull request.
4. Open as a draft until the content is complete, then mark it ready for review.
5. When review comes back, apply every BLOCKING item or reply in its thread explaining why not. Reply to every thread. Do not resolve threads you did not open; the reviewer or Justin resolves them.

## Carrying an agent's work

Some sessions cannot push to some repositories. Claude's cloud sessions, for example, cannot push to any repository whose name begins with a dot, including this one. In that case the agent drafts the files and Justin carries them. Steps, in order:

1. The agent sends every file, the commit title and description, and the pull request title and body. The commit description names the drafter, any editors, and who uploaded, and ends with a co-author line for each contributing agent:
   `Co-Authored-By: jhilliardx-claude-ai <347296035+jhilliardx-claude-ai@users.noreply.github.com>`
   Each trailer is on its own line, with angle brackets, at the very end.
2. Justin uploads the root files with Add file, then Upload files, onto a new branch under his prefix (`jhilliardx/<purpose>`). The web uploader flattens folders, so files in a subfolder are added afterward with Add file, then Create new file, typing the full path (for example `profile/README.md`) and committing to the same branch.
3. Propose changes creates the branch, not the pull request. Click Create pull request and confirm a pull request number exists.
4. The reviewer reviews under the rules below.
5. Justin squash-merges and replaces GitHub's default squash message, which stacks every branch commit message, with the clean title and description from step 1. The branch commit messages do not survive a squash; the merge message does.

## Reviewing a pull request

Read the pull request body first: it names the review shape and the one question. Review only against that shape. Post one response per review round, then stop. After corrections, a new review round may verify the changes and update the verdict.

For `cross-read`, answer only the requested comparison question as a list. Do not rank the drafts or include BLOCKING, NON-BLOCKING, or a verdict. Submit it as a Comment review; a cross-read is not merge approval.

For `ready-to-publish` and `governance`, use this structure:

```
SHAPE: <ready-to-publish | governance>

BLOCKING
- <file and line>: <what is wrong> -> <what to change>
(or "None.")

NON-BLOCKING
- <file and line>: <suggestion>
(or "None.")

ANSWER TO THE QUESTION
<one paragraph>

VERDICT: <approve as is | request changes>
```

For `governance`, add this line immediately before VERDICT: "What this lets an agent do that it could not do before: <answer, or None>."

BLOCKING means the pull request should not merge without the change. Everything else is NON-BLOCKING. Do not pad either list. Any unresolved BLOCKING finding requires the verdict `request changes` and the GitHub review event Request changes. With no blocking findings, use `approve as is` and Approve; non-blocking suggestions do not prevent approval.

### Review shapes

| Shape | Use for | Reviewer checks |
| --- | --- | --- |
| ready-to-publish | Documents and pages a stranger will read | Accuracy against sources, clarity for a cold reader, claims that overreach, rule 12 |
| governance | Anything that changes rules, permissions, templates, or workflows | Everything in ready-to-publish, plus one required line: "What this lets an agent do that it could not do before." |
| cross-read | Comparing independent drafts of the same thing | One question only: what did the other drafts get right that this one missed? No ranking. |

## After merge

The reviewer opens at most one follow-up issue collecting the NON-BLOCKING items that were not applied, titled `Follow-ups: <pull request title>`, linking the pull request. If there are none, no issue.

## What this file does not cover

Repository-specific rules live in each repository's own `AGENTS.md`, which adds to this file and never loosens it.

---

**Authors:** Justin Hilliard and Claude (Anthropic).
**Reviewers/editors:** Justin Hilliard and ChatGPT (OpenAI).
