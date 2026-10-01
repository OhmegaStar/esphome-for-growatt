# Project Instructions

## Project Decisions
- The fallback captive-portal password is intentional and is not considered a security issue for this project. Do not flag it unless the configuration or threat model changes. Do not record the password itself here.

## Commit Messages
- Write commit messages for human readers. Use a specific subject that describes the change, and add a concise body when it helps explain why or clarify scope. Use bullet lists for listing several distinct changes that need listing. use sections to separate different types of changes. Use the imperative mood in the subject line, e.g., "Add feature" instead of "Added feature" or "Adding feature".

## Release Notes
- Release notes are generated from commit messages. Use the `\.\tools\release.ps1` script to create a release commit and tag, then push both. GitHub Actions will publish a GitHub Release with generated release notes when the tag is pushed. Omit `-Push` to review the commit and tag before pushing them manually. Combine the commit messages for all changes since the previous release into a single release note. Use bullet lists for listing several distinct changes that need listing. use sections to separate different types of changes. Use meaningful icons such as ✅, ⚠️, 🛠️, and 🔧 when they improve clarity, but keep them consistent and concise so the notes remain easy to scan.

## Maintaining These Instructions
- When a lasting project preference or decision is established, add a concise, actionable rule here. Do not record secrets or temporary task details. if uncertain, ask the team for consensus before adding a rule. If a rule is later found to be unnecessary or counterproductive, remove it. ask the team for consensus before removing a rule.