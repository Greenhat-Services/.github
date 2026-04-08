# Greenhat Services — GitHub Configuration

This repository contains org-wide GitHub configuration, templates, and workflow 
standards for Greenhat Services.

It is not a codebase. Do not use it for client or project work.

---

## What's in here

### Issue Templates
Standardised issue templates used across all Greenhat repositories. All new work 
requests should use the appropriate template to ensure consistent triage and 
agent-ready formatting.

### Labels
The canonical label set for all Greenhat repositories. Labels are defined here 
and mirrored across repos using the GitHub CLI clone script below.

### Workflow Standards
Documents the Greenhat GitHub Projects workflow including board structure, triage 
process, and agent-ready criteria.

---

## Board Structure

All new work enters the **Greenhat Intake** board at org level. Directors triage 
and route issues to the relevant per-repo project board from there.

| Board | Purpose |
|---|---|
| Greenhat Intake | Master intake and triage for all incoming work |
| Per-repo boards | Active development tracking per client or codebase |

---

## Label Taxonomy

Labels are consistent across all repos. The full set is maintained on this repo 
and cloned to others using:
```bash
gh label clone greenhat-services/.github --repo greenhat-services/[target-repo] --force
```

Key labels:

| Label | Purpose |
|---|---|
| `triage` | Newly arrived, not yet reviewed by a director |
| `agent-ready` | Scoped and structured for agent or Claude Code pickup |
| `priority: critical` | Same-day response required |
| `priority: high` | Current sprint |
| `priority: normal` | Standard queue |
| `priority: low` | Backlog |

---

## Triage Process

1. New issues arrive in **Greenhat Intake → Inbox** via Power Automate or manual entry
2. Directors review daily and move to **Triage**
3. Issue is scoped, labelled, estimated (points), and assigned to a client/repo
4. Once acceptance criteria are complete, label as `agent-ready` and move to **Ready**
5. Developer or agent picks up from **Ready**

---

## Maintaining This Repo

- Label changes must be made here first, then cloned out
- Issue template changes are applied org-wide automatically
- Workflow documentation should be kept current as processes evolve

*Maintained by Greenhat Services.*
