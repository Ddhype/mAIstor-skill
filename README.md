# mAIstor onboarding skill — install for Claude

This folder contains **`SKILL.md`**, instructions the model follows when helping someone enter **mAIstor learning mode** (track selection, onboarding, lessons).

## Prerequisites

- A **mAIstor account** (via the web app / Supabase auth) and **mAIstor MCP** connected in Claude (OAuth). Step-by-step for both is in the skill body and in detail in [`../../CLAUDE_CONNECTOR.md`](../../CLAUDE_CONNECTOR.md).

## Install without manual upload

1. **Public mirror repo (recommended if this monorepo is private)**  
   Follow [`SYNC_PUBLIC_REPO.md`](SYNC_PUBLIC_REPO.md). Use the **raw GitHub URL** to `SKILL.md` in the public repo (Claude → Skills / import from URL, if available).

2. **HTTPS (Vercel web app in this monorepo)**  
   After deploy, fetch:  
   `https://<your-vercel-domain>/skills/mAIstor-onboarding`  
   Same markdown as `SKILL.md` — save or point your client at this URL.

3. **This repo is public**  
   You can use a raw URL into this monorepo, e.g.  
   `https://raw.githubusercontent.com/<org>/<repo>/main/docs/skills/mAIstor-onboarding/SKILL.md`

## Legacy: paste / upload

If your client has no URL import: create a skill or project and **paste** the contents of **`SKILL.md`**, or upload the file.

## Updating

When MCP tool names or onboarding copy change, edit **`SKILL.md`** here and merge to **`main`**. If you use the **public mirror**, GitHub Actions ([`.github/workflows/mirror-maistor-skill.yml`](../../../.github/workflows/mirror-maistor-skill.yml)) copies `SKILL.md` to that repo automatically — see [`SYNC_PUBLIC_REPO.md`](SYNC_PUBLIC_REPO.md) for secrets and variables. Keep **`docs/onboarding/CLAUDE_ONBOARDING_PROMPT.md`** as the detailed onboarding script; this skill stays a short orchestration layer.
