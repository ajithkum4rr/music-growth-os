# Music Growth OS — Usage Guide

## Purpose

This guide explains how to use the Music Growth OS repository:
- where to start
- how to follow the manual docs
- how to use agents
- how to introduce automation
- where the key files and folders belong

## System overview

This repo is already built with all 26 phases and the supporting agent definitions:
- `docs/` contains the phase-level manuals and playbooks.
- `agents/` contains the agent role guides and definitions.
- `templates/`, `checklists/`, `sops/`, `analytics/`, `campaigns/`, `experiments/`, `rag/`, and `research/` contain supporting execution assets.

## Core flow

Use this note as the system map:

```
                       MUSIC GROWTH OS
                       │
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
     STRATEGY       DOCUMENTATION   DATA
        │              │              │
        ▼              ▼              ▼
    26 PHASES        SOPs         ANALYTICS
                       │              │
                       ▼              ▼
                   TEMPLATES       METRICS
                       │              │
                       └──────┬───────┘
                              ▼
                         AUTOMATION
                              │
                              ▼
                           AI / RAG
                              │
                              ▼
                           AGENTS
                              │
                              ▼
                       FUTURE SYSTEM
```

This diagram shows the repo architecture and the order of execution:
1. Define strategy and phase plans.
2. Capture the process inside documentation and SOPs.
3. Track performance with analytics and metrics.
4. Use templates to execute faster.
5. Build automation after the manual process is proven.
6. Add AI/RAG support and agent workflows when the system is stable.

## Where to start

### 1. Start with the guide

Read `USAGE-GUIDE.md` first. This file explains how the repo is organized and how to choose a path.

### 2. Read the overview files

- `README.md` — general project orientation.
- `MASTER-PLAN.md` — system architecture and phase dependencies.
- `ROADMAP.md` — suggested short-term launch plan.
- `PROJECT-STARTER.md` — first execution tasks.
- `CURRENT-RELEASE.md` — live release tracker for the active campaign.

### 3. Start the manual doc flow

If you want to execute manually, follow this path:

1. Open `docs/README.md` to see the phase index.
2. Work phase-by-phase in order from `docs/00-foundation/` through `docs/26-repeatable-playbook/`.
3. Use each phase's `README.md` and supporting docs for the steps, checklists, and templates.
4. Use `templates/` and `checklists/` for reusable forms and execution tools.
5. Update `CURRENT-RELEASE.md` as you make progress.

### 4. If you want to use agents

The agent system is designed to support your manual work, not replace it.

1. Start by reading `agents/README.md`.
2. Use this repo to tell the agent what phase or task you want help with.
3. Open the relevant agent file in `agents/` for the agent’s role and scope.
4. Ask the agent to:
   - summarize a phase or checklist
   - generate ideas from your research
   - create drafts for outreach, social, or campaign briefs
   - review your plan and suggest optimizations
5. Always validate agent output against the manual docs and your brand.

### 5. If you want to add automation

Automation belongs after the manual process is working.

1. Read `docs/23-automation/README.md` and its supporting guides.
2. Build automation for repeatable and low-risk tasks first:
   - reporting exports
   - email follow-up reminders
   - campaign check-ins
3. Use `templates/automation-roadmap-template.md`, `docs/23-automation/03-automation-checklist.md`, and `docs/23-automation/04-automation-prioritization-guide.md` to choose what to automate.
4. Keep automation rules simple and easy to update.

## Manual vs agent workflow

### Manual execution

Best when you want full control and want to learn the process. Follow the phase docs directly and use the templates to capture your work.

### Agent-assisted execution

Best when you want faster idea generation, structured summaries, or a second set of eyes. Use agents as assistants, not decision makers.

### Automation

Best when you have repeatable tasks and verified processes. Start automation only after the manual workflow is stable.

## How to use this repo effectively

- Use `CURRENT-RELEASE.md` as your campaign command center.
- Keep the docs and templates open side-by-side with your work.
- Track progress across phases in the table inside `CURRENT-RELEASE.md`.
- Use `checklists/` for day-to-day execution.
- Use `experiments/01-experiments-log.md` for optimization testing.
- Use `analytics/01-analytics-overview.md` as your data anchor.
- Use `rag/01-rag-readme.md` to manage AI/RAG sources and prompts.
- Use `research/01-research-roadmap.md` to capture gaps and next questions.

## All phases and agents are already created

This repository already includes:
- 26 phase folders under `docs/`
- a starter doc for every phase
- supporting SOPs, templates, checklists, and launch assets
- a full agent folder with specific agent roles in `agents/`

If you want to begin manually, start with `docs/00-foundation/README.md` and `PROJECT-STARTER.md`.
If you want to begin with agent assistance, read `agents/README.md` and choose the agent that matches your current phase.

## Recommended first actions

- update `CURRENT-RELEASE.md` with your release name, date, and objectives
- complete Phase 0 foundation setup
- define your artist positioning and visual direction in Phase 1
- map your audience in Phase 2
- use the current phase table in `CURRENT-RELEASE.md` to track progress

## Notes

- The system is designed to be used by a single artist or small team.
- The human process always comes first; automation and agents are tools that support execution.
- Keep the diagram and flow in mind as you move from strategy to documentation to data to automation to AI.
