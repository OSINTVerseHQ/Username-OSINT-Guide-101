# Contributing

This repository is a living **username OSINT** field manual. Fixes and additions are welcome.

## What to send

- Dead tools, moved URLs, or site-check modules that now false-positive
- Platform handle-rule changes (length, allowed characters, vanity URLs)
- Techniques that stay on the lawful, passive side of the line
- Corrections to confidence rules, legal notes, or worked examples

## What we will not merge

- How to access accounts, impersonate, or complete password resets
- Credential stuffing or “try the username as the password”
- Bulk scraping / contact-sync enumeration scripts
- Anything that helps stalk, harass, or impersonate a person
- Unsourced tool dumps with no investigative question

## How to edit

1. Fork the repo and branch from `main`
2. Keep the voice: field manual, not marketing
3. Prefer a concrete claim + source + caveat over another bullet list
4. Update the [checklist](docs/checklist.md) if you add a step people should always run
5. Open a pull request with a short “why”

## Style

- Original prose. Do not paste another site’s guide
- Name the tool, the question it answers, and the failure mode
- Always treat a username *hit* as a lead, not an identity
- Relative links between files in this repo

Questions: [hi@osintverse.com](mailto:hi@osintverse.com)
