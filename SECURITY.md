# Security

## Reporting a vulnerability

Report it privately through GitHub: open the repository's **Security** tab and choose **Report a vulnerability**. Do not open a public issue describing a security problem.

If the Security tab shows no **Report a vulnerability** option, private reporting is not yet enabled for that repository. Open an issue that says only that you have a security report and need a private contact, with no details.

Justin Hilliard reviews every report and decides on every fix. Fixes go through the normal pull request process.

## What we do by default

- No credentials, tokens, or private personal information in any repository. Secret scanning and push protection are on.
- Default branches are protected: no direct pushes, no force pushes, and every change goes through a pull request requiring one approval. The organization admin can merge without that approval; agents cannot.
- Agent accounts hold no bypass of these rules.
