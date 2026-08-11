---
title: "LinkedIn Outreach Competitive Teardown"
date: "2026-08-09"
author: ""
last_audited: "2026-08-09"
tags: ["linkedin", "research", "competitive", "outreach", "saas"]
status: active
sources:
  - https://expandi.io/
  - https://expandi.io/pricing/
  - https://dripify.com/
  - https://dripify.com/pricing/
  - https://www.smartlead.ai/
  - https://www.smartlead.ai/pricing
  - https://www.heyreach.io/
  - https://www.heyreach.io/pricing
  - https://salesflow.io/
  - https://salesflow.io/pricing
  - https://salesflow.io/features
  - https://www.lagrowthmachine.com/
  - https://www.lagrowthmachine.com/pricing/
  - https://www.lagrowthmachine.com/linkedin-safety/
references:
  - Ideas/linkedin-outreach-assistant
---

<!--
Competitive teardown of LinkedIn/email outreach automation vendors for a
compliance-first LinkedIn outreach campaign-builder. Per-tool detail lives in
tool-profile-*.md sub-notes; this note holds the cross-cutting picture.
Evidence only: vendor claims are QUOTED/claimed; judgments are labelled analysis.
-->

## Question

Who are the realistic competitors for a compliance-first LinkedIn outreach
campaign-builder; how do they position; which channels (LinkedIn-native vs
email-first) do they cover; what safety/compliance language do they use; what
features and pricing do they offer?

## Hypothesis

Expect a split into (a) LinkedIn-native automation tools and (b) email-first
cold-outreach tools, with entry pricing clustered around $39–$99/mo and
"compliance" marketed as anti-ban/account-safety rather than regulatory
compliance (consent, lawful basis, deliverability law).

## Log / Findings

- 2026-08-09 — Fetched official home + pricing pages for all six vendors;
  salesflow.io answered 403 to direct fetch, so its content was captured via
  a live search index of the official pages (noted in its profile).

### Summary grid

| Tool | Category | Channels | "Safety" frame | Entry price | Sub-note |
|---|---|---|---|---|---|
| Expandi | LinkedIn-native + email follow-up | LI-native,email | Anti-ban: dedicated country IP, warm-up, hard limits | $99/mo/account | [[tool-profile-expandi.md]] |
| Dripify | LinkedIn-native + email | LI+email (same seq.) | Anti-ban: dedicated IP, human-like timing, adaptive control | $59/mo/user | [[tool-profile-dripify.md]] |
| Smartlead | Email-first | Email (unlimited boxes), calls | Deliverability/reputation (avoid spam) | $39/mo | [[tool-profile-smartlead.md]] |
| HeyReach | LinkedIn-native multi-account | LI-native; email via Instantly/Smartlead | Anti-ban: sender daily limits, proxies | $79/mo/sender | [[tool-profile-heyreach.md]] |
| Salesflow | LinkedIn-native + email | LI+email (Dynamic Outreach) | Anti-ban: cloud, dedicated IP, auto-withdrawal, "near 0% ban" | $99/seat | [[tool-profile-salesflow.md]] |
| LaGrowthMachine | Multichannel native | LI+email+X+calls | Anti-ban + explicit GDPR section | €60/mo/identity | [[tool-profile-lagrowthmachine.md]] |

### Cross-cutting findings

- "Safety" in this category is overwhelmingly anti-ban engineering (dedicated
  IPs/proxies, warm-up, randomized timing, daily limits), not regulatory
  compliance. LGM is the only vendor of the six with an on-page GDPR statement;
  Smartlead frames safety as email-reputation/deliverability. (analysis)
- None of the six productize consent management, lawful-basis selection, or
  unsubscribe tooling — the natural positioning wedge for a compliance-first
  builder. (analysis)
- All six operate automation that violates LinkedIn's Terms of Service; footers
  disclaim it ("Use of Expandi is at your own risk"; "HeyReach is not
  associated with, or endorsed by, the LinkedIn Corporation"). (analysis)
- Feature parity is high: sequences with conditions/branching, AI
  personalization variables, unified inbox, CRM sync, team management are table
  stakes across LinkedIn-native tools. (analysis)
- Entry pricing clusters at $39–$99/mo per user/account; agency/scale tiers
  (HeyReach, Salesflow, Expandi) jump to $999+/mo or require sales calls. (analysis)
- Email-first (Smartlead) vs LinkedIn-native (Expandi/Dripify/HeyReach/
  Salesflow) is the sharpest category split; LGM and Dripify run both channels
  natively in one sequence. (analysis)

## Sources

- https://expandi.io/ · https://expandi.io/pricing/
- https://dripify.com/ · https://dripify.com/pricing/
- https://www.smartlead.ai/ · https://www.smartlead.ai/pricing
- https://www.heyreach.io/ · https://www.heyreach.io/pricing
- https://salesflow.io/ · https://salesflow.io/pricing · https://salesflow.io/features
  (fetched via search index; see profile)
- https://www.lagrowthmachine.com/ · https://www.lagrowthmachine.com/pricing/ ·
  https://www.lagrowthmachine.com/linkedin-safety/

## Changelog

- 2026-08-09 — Created.
- 2026-08-09 — Initial competitive teardown complete.