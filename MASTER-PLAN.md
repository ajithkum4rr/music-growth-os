# MASTER PLAN

## Executive overview

This repository is a living, practical Music Growth OS for `ajkay`.

The objective is to build a repeatable, measurable, and legitimate music marketing system that can be executed by a single independent artist.

The system is built around:

- Audience discovery and targeting
- Content creation and distribution
- Digital infrastructure and analytics
- Organic growth and paid advertising
- Playlist and PR outreach
- Release campaign execution
- Measurement, optimization, and retention
- Automation, AI, and future scaling

## Core architecture

### Major components

1. Foundation
2. Artist brand & positioning
3. Audience research
4. Release preparation
5. Content system
6. Digital infrastructure
7. Organic social strategy
8. Meta advertising
9. Retargeting
10. Spotify growth & analytics
11. Playlist outreach
12. Spotify editorial pitching
13. YouTube strategy
14. TikTok strategy
15. Landing page & fan funnel
16. Email list and fan capture
17. PR / press outreach
18. Blog / media / publicity
19. Collaborations & networking
20. Release campaign execution
21. Analytics & attribution
22. Campaign optimization
23. Fan retention
24. Automation
25. AI / RAG / agents
26. Post-campaign analysis
27. Repeatable release playbook

### Why this sequence

- Early phases build the identity, research, and infrastructure needed for later campaigns.
- Paid media and outreach work better when the brand, audience, and release plan are clear.
- Analytics and optimization depend on measurable systems built in the first half.
- Automation and AI should be introduced only after the process has been documented and repeated.

## Phase dependency graph

### Base dependency ordering

- `Phase 0` must come first.
- `Phase 1` and `Phase 2` are parallel but both feed Phase 3.
- `Phase 3` is required before many content, landing page, email, and outreach actions.
- `Phase 4`, `Phase 5`, and `Phase 6` create the execution engine for organic and paid tactics.
- `Phase 7` and `Phase 8` depend on infrastructure and early content.
- `Phase 9` and `Phase 11` depend on Spotify account setup and release readiness.
- `Phase 15` and `Phase 16` run alongside release execution and retention.
- `Phase 24` is a later stage built on documented workflows and campaign data.

### Graph view

```
Phase 0 -> {Phase 1, Phase 2}
{Phase 1, Phase 2} -> Phase 3
Phase 3 -> {Phase 4, Phase 5, Phase 6}
{Phase 4, Phase 5, Phase 6} -> Phase 7
Phase 7 -> Phase 8
Phase 5 -> Phase 9
Phase 3 -> Phase 10
Phase 5 -> Phase 11
{Phase 4, Phase 5, Phase 9, Phase 11} -> Phase 14
Phase 5 -> Phase 12
Phase 5 -> Phase 13
Phase 14 -> Phase 15
{Phase 7, Phase 9, Phase 10, Phase 11, Phase 12, Phase 13, Phase 14, Phase 15, Phase 16} -> Phase 19
Phase 19 -> {Phase 20, Phase 21, Phase 22}
{Phase 20, Phase 21} -> Phase 23
Phase 23 -> Phase 24
Phase 19 -> Phase 25
Phase 25 -> Phase 26
```

## Documentation architecture

This repo is organized for clarity, accountability, and reuse.

### Top-level docs

- `README.md`: overview, structure, and starting point.
- `MASTER-PLAN.md`: strategy, dependencies, architecture.
- `ROADMAP.md`: execution timeline.

### Phase docs

`/docs/00-foundation` through `/docs/26-repeatable-playbook` hold phase-level SOPs.
Each folder should contain at least one `README.md` describing the phase and the next actions.

### Supporting sections

- `/sops`: repeatable SOPs for marketing campaigns, playlist outreach, PR, email funnels, and analytics.
- `/templates`: structured templates for campaigns, outreach, creative briefs, and reporting.
- `/checklists`: execution checklists for each phase and critical task.
- `/research`: notes for audience research, competitor analysis, and artist comparisons.
- `/campaigns`: release campaign plans, results, and post-mortem notes.
- `/analytics`: metric definitions, dashboards, and attribution models.
- `/experiments`: experiments, hypotheses, outcomes, and decisions.
- `/agents`: AI agent definitions and human-in-the-loop guardrails.
- `/rag`: knowledge source design for retrieval-augmented workflows.
- `/scripts`: small automation scripts and data helpers.
- `/data`: simple structured tracking tables in CSV/JSON.

## Agent architecture

Agents should be designs, not autonomous control systems at first.

Each agent definition should include:

- Name
- Purpose
- Responsibilities
- Inputs
- Outputs
- Required knowledge
- Tools / data sources
- Workflow
- Decision rules
- Safety rules
- Platform policy constraints
- Human approval required
- Failure handling
- Example tasks
- RAG sources
- What the agent must never do

### Initial agent categories

- `audience-research-agent`
- `content-strategy-agent`
- `meta-ads-agent`
- `spotify-analytics-agent`
- `playlist-outreach-agent`
- `pr-outreach-agent`
- `release-campaign-agent`
- `analytics-agent`
- `optimization-agent`
- `fan-retention-agent`

### Agent operating principle

- Human first.
- Agents should suggest, summarize, and flag actions.
- Agents must not execute paid changes, send mass outreach, or spend budget without explicit approval.
- Agents should support documentation, not replace judgment.

## RAG architecture

A retrieval-augmented workflow is future-facing.

### Source hierarchy

- `TIER 1`: Official platform documentation (Meta, Spotify, YouTube, TikTok, email providers)
- `TIER 2`: Official creator/business documentation (Spotify for Artists, Meta for Creators, Google Ads Help)
- `TIER 3`: Reliable industry research (music marketing reports, case studies, independent creator insights)
- `TIER 4`: Community discussions and anecdotal experience (Reddit, forums, podcasts) — label as anecdotal and verify before use

### RAG sources

- `docs/` phase playbooks
- `research/` audience and campaign research
- `analytics/` historical metrics and dashboards
- `campaigns/` results and post-mortems
- Official help center articles and platform policy references

### RAG design

- Use structured markdown and CSV/JSON for first-party data.
- Keep source metadata simple: title, source, date, importance.
- Prioritize first-party data over third-party anecdotes.
- Label uncertain or time-sensitive content with `VERIFY CURRENT`.

## Data architecture

Start small.

### Core entities

- `artists`
- `songs`
- `releases`
- `campaigns`
- `audiences`
- `creatives`
- `ads`
- `playlists`
- `curators`
- `press_contacts`
- `press_outreach`
- `social_posts`
- `metrics`
- `experiments`
- `fans`
- `email_subscribers`

### Storage approach

- Use CSV/JSON/Markdown for early tracking.
- Prefer human-readable, version-controlled tables.
- Add lightweight scripts only when repetitive exports are needed.
- Use a real database only when the CSV/JSON model becomes too slow or error-prone.

### Example storage rules

- `data/songs.csv`
- `data/releases.csv`
- `data/campaigns.csv`
- `data/playlist-curators.csv`
- `data/press-outreach.csv`
- `data/metrics-weekly.csv`
- `data/experiments.csv`
- `data/email-subscribers.csv`

## Analytics architecture

### Metrics categories

- Discovery: impressions, reach, traffic sources
- Engagement: clicks, views, watch time, saves, follows
- Conversion: landing page visits, stream listeners, email signups
- Retention: repeat streams, profile visits, playlist adds
- Cost: CPM, CPC, cost per listener, cost per follower
- Quality: save rate, follow rate, completion rate, repeat listener rate

### Attribution model

- Directly measurable: ad sources, channel referrals, landing page events
- Inferred: playlist discovery, algorithmic Spotify sources, organic social influence
- Unknown: offline word-of-mouth, untagged shares, cross-device attribution gaps

### Dashboard design

- Track source-to-stream conversion
- Track funnel progression from content to listens to follows
- Compare cost against value metrics
- Use first-party analytics where available and annotate limitations

## Automation architecture

### Early automation targets

- Weekly analytics summaries
- UTM generation for campaigns
- Report templates
- Playlist/outreach tracking updates
- Email campaign prep reminders
- Content calendar scaffolding

### Human-in-the-loop tasks

- Creative review
- Ad budget changes
- Outreach emails
- PR pitches
- Release decisions

### Manual-only tasks

- Song quality assessment
- Brand voice definition
- Relationships and networking
- Editorial pitch writing
- Strategy decisions

## Security architecture

- Never store passwords or API keys in this repo.
- Use `.env.example` for configuration samples.
- Use 2FA on all accounts.
- Apply least privilege to ad accounts, email providers, and analytics tools.
- Keep account ownership under your name or trusted manager.
- Back up critical account information in a secure password manager.

## Recommended order of execution

1. `Phase 0 — FOUNDATION`
2. `Phase 1 — ARTIST BRAND & POSITIONING`
3. `Phase 2 — AUDIENCE RESEARCH`
4. `Phase 3 — MUSIC & RELEASE PREPARATION`
5. `Phase 5 — DIGITAL INFRASTRUCTURE`
6. `Phase 4 — CONTENT SYSTEM`
7. `Phase 6 — ORGANIC SOCIAL STRATEGY`
8. `Phase 9 — SPOTIFY GROWTH & ANALYTICS`
9. `Phase 7 — META ADVERTISING`
10. `Phase 8 — RETARGETING`
11. `Phase 10 — LEGITIMATE PLAYLIST OUTREACH`
12. `Phase 11 — SPOTIFY FOR ARTISTS PITCHING`
13. `Phase 12 — YOUTUBE STRATEGY`
14. `Phase 13 — TIKTOK STRATEGY`
15. `Phase 14 — LANDING PAGE / FAN FUNNEL`
16. `Phase 15 — EMAIL LIST & FAN CAPTURE`
17. `Phase 16 — PR / PRESS OUTREACH`
18. `Phase 19 — RELEASE CAMPAIGN EXECUTION`
19. `Phase 20 — ANALYTICS & ATTRIBUTION`
20. `Phase 21 — CAMPAIGN OPTIMIZATION`
21. `Phase 22 — FAN RETENTION`
22. `Phase 23 — AUTOMATION`
23. `Phase 24 — AI / RAG / AGENT SYSTEM`
24. `Phase 25 — POST-CAMPAIGN ANALYSIS`
25. `Phase 26 — REPEATABLE RELEASE PLAYBOOK`

## What to avoid yet

- Do not buy playlist placements from services that promise guaranteed streams.
- Do not use click farms, bot streams, or fake engagement.
- Do not start paid advertising without a landing page or brand assets.
- Do not automate messaging or budget changes without manual approval.
- Do not assume any platform UI or policy is static — verify current documentation.

## Minimum viable version

A lean MVP for the first release includes:

- `Phase 0` foundation checklist complete
- `Phase 1` basic artist positioning
- `Phase 2` audience research notes
- `Phase 3` release plan and asset list
- `Phase 5` accounts created and linked
- `Phase 6` social content plan in place
- `Phase 9` Spotify for Artists set up
- `Phase 14` simple landing page with track links and email signup
- `Phase 15` email capture and welcome message
- `Phase 19` a release campaign execution plan
- `Phase 20` analytics tracking plan

## Future advanced version

A stronger version adds:

- full funnel retargeting from cold to fans
- multi-platform creative testing
- legitimate playlist outreach system
- PR and press outreach workflows
- automated reporting and performance summaries
- an early AI/RAG agent to summarize metrics and suggest experiments
- repeatable release playbook with post-campaign review

## Next step

Open `docs/00-foundation/README.md` and start Phase 0.
