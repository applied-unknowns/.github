# .github

Organization defaults for Applied Unknowns. This repository is special to GitHub: some files here apply to every repository in the organization, and some apply only here.

## What is in this repository

| Path | What it does | Applies to |
| --- | --- | --- |
| `profile/README.md` | The public page shown at github.com/applied-unknowns | The organization page |
| `AGENTS.md` | Rules for every agent: identities, rules, authoring, carrying work, the review format | Read by agents directly; GitHub does not copy it into other repositories |
| `CLAUDE.md` | Points Claude Code to `AGENTS.md` | This repository |
| `GOVERNANCE.md` | Who decides, how rules change, the permission ladder | Organization policy, read by reference. Not a GitHub default; it is not applied to other repositories. |
| `CONTRIBUTING.md` | How to take part, and why outside pull requests wait for now | Every repository without its own (community health file) |
| `SECURITY.md` | How to report a vulnerability privately | Every repository without its own (community health file) |
| `CODE_OF_CONDUCT.md` | Expected conduct for people and agents | Every repository without its own (community health file) |
| `PULL_REQUEST_TEMPLATE.md` | The default pull request body | Every repository without its own |
| `CODEOWNERS` | Names Justin as the reviewer for rule files | This repository only |

The organization's working records (open items, backlog, lessons, and the repository index) live in the [`foundation`](https://github.com/applied-unknowns/foundation) repository, so agents can update them without carrying files into this one.

## What does not carry over

GitHub uses defaults from this repository for supported community health files (such as pull request templates and issue templates) when a repository lacks its own. These defaults are not copied into the receiving repository's files or history. It does not copy `AGENTS.md`, `CODEOWNERS`, licenses, or rulesets. Each repository therefore carries its own `AGENTS.md`, which points back to the one here and adds to it, never loosening it. Rulesets are set at the organization level in GitHub settings, not in files.

## How changes are made

Through a branch and a pull request, reviewed under the format in `AGENTS.md`, merged by Justin. Direct pushes to `main` are blocked by the organization ruleset. As organization admin, Justin can merge a pull request without its required approvals; he cannot push directly to main. Required code-owner approvals are not yet enabled; `CODEOWNERS` prepares for that enforcement.

---

**Authors:** Justin Hilliard and Claude (Anthropic).
**Reviewers/editors:** Justin Hilliard and ChatGPT (OpenAI).
