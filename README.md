# Consumption Reporting Gateway

A minimal public sign-in gateway for a private Customer Success Architect
consumption-reporting workspace.

Maintained by David Liu, Customer Success Architect.

## What this repository contains

This repository publishes **one static page whose only job is to hand a visitor
off to Microsoft authentication**. It deliberately contains:

- no customer or account names
- no account, opportunity or milestone identifiers
- no commercial, licensing or compliance status
- no metrics of any kind

All reporting content lives in Microsoft OneDrive for Business and is reachable
by signed-in Microsoft employees through organization-scoped, read-only sharing
links. Public and guest access are not enabled. The account
launcher itself (`hub.html`) is stored alongside the dashboards in OneDrive and
is **not** published here.

## Access

The primary button opens the shared reporting folder using its **People in
Microsoft / Can view** link. Visitors should open that folder first, then open
`hub.html`, so supporting files, archives and backups are accessible as well.
The secondary launcher link includes its own organization-only sharing token.
Use an `@microsoft.com` work account.

Preserve the `share` query parameter when updating either link. A copied owner
navigation URL without that parameter does not grant access to a new visitor.
Separately permissioned dashboard entry pages must retain their own
organization-scoped view links. Linked Teams conversations, MSX records and
MSXi reports remain subject to those services' permissions.

## Terminology

- **PRU** — Power/Repeat Users, the engaged-usage measure shown on the dashboards.
- **MAU** — monthly active users of Copilot agents.

## Tech stack

- HTML5 / CSS3 / vanilla JavaScript
- Static single page — no build step

## Run locally

Open `index.html` directly in a browser, or serve it:

```bash
python -m http.server 8000
```

## Contribution rule

Do not add customer names, account identifiers, deal status, compliance posture
or contact details to any file in this repository. Those belong in the
OneDrive-hosted launcher only. Git history is permanent and public.
