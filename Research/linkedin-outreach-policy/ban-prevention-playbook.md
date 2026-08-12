---
title: "LinkedIn Ban-Prevention Playbook (Vendor-Documented)"
date: 2026-08-12
author: ""
last_audited: 2026-08-12
tags: ["linkedin","research","ban-prevention","account-safety","automation"]
status: active
sources:
  - https://www.linkedin.com/help/linkedin/answer/a1341387
  - https://www.linkedin.com/help/linkedin/answer/a1340567
  - https://www.prosp.ai/blog/linkedin-outreach-without-getting-restricted
  - https://help.prosp.ai/en/articles/10348233-connect-a-linkedin-profile-using-credentials
  - https://dripify.com/linkedin-detection-system/
  - https://dripify.com/features/extra-safety-algorithm/
  - https://expandi.io/blog/linkedin-account-restricted/
  - https://www.lagrowthmachine.com/linkedin-safety/
  - https://www.heyreach.io/pricing/
  - https://northlight.ai/blog/linkedin-account-restricted-fix
  - https://prospectingmanual.com/linkedin-automation/troubleshooting/account-restriction-warnings/
  - https://www.leadloft.com/blog/linkedin-limits
references: ["Research/linkedin-outreach-policy/linkedin-outreach-policy.md"]
---

## Purpose

Operational sub-note of the LinkedIn Outreach Policy workspace: what LinkedIn
and third-party tools document about why automated accounts get flagged, and
how an outreach system should be built to hold accounts safely. A companion
to [[connection-request-limits]] and [[messaging-limits]]; limit numbers live
there. All figures are heuristics or vendor claims, not LinkedIn guarantees.
The Source of Truth rule applies: nothing here is presented as official unless
marked official.

## How automated activity is detected

- Detection uses technical signals AND behavioral patterns, not just volume. (vendor-documented: [Dripify LinkedIn detection system](https://dripify.com/linkedin-detection-system/))
- Technical signals: datacenter IPs; geographic or IP mismatch (login while the IP reports another country); multiple simultaneous logins from different IPs; rotating IPs; browser extensions that inject scripts or modify the page; traffic from servers LinkedIn does not recognize as the user's device. (vendor-documented: [Dripify](https://dripify.com/linkedin-detection-system/); [Expandi](https://expandi.io/blog/linkedin-account-restricted/))
- Behavioral signals: fixed-interval actions firing like clockwork; bot-speed repetitive sends; identical templated messages at scale; automation running while the user is offline or asleep; sudden spikes off an account's own baseline; messaging immediately after connecting; bulk endorsing or following in minutes. (vendor-documented: [Dripify](https://dripify.com/linkedin-detection-system/); [Expandi](https://expandi.io/blog/linkedin-account-restricted/))
- Official: LinkedIn prohibits circumventing use limits on search results, profiles, or videos, plus all automated access, scraping, and UI-modifying extensions — [Help a1341387](https://www.linkedin.com/help/linkedin/answer/a1341387). After an automated-activity restriction, disabling the software auto re-enables the account at the time given in the suspension notice, and LinkedIn recommends changing your password regularly — [Help a1340567](https://www.linkedin.com/help/linkedin/answer/a1340567). (official)

## Warm-up and ramp (proactive)

- New or dormant accounts: warm up 3-4 weeks before outreach — complete the profile, log in regularly, post or comment, engage with content; do not jump from zero activity into a full push. (vendor-documented: [Prosp blog](https://www.prosp.ai/blog/linkedin-outreach-without-getting-restricted))
- Ramp gradually off the account's own baseline: start new accounts at 5-10 invites/day and increase roughly 10-20% per week; sudden spikes after quiet periods flag even safe-looking volumes. (vendor-documented: [Prosp blog](https://www.prosp.ai/blog/linkedin-outreach-without-getting-restricted))
- Post-restriction recovery ramps ~10-20 invites/week over 4-6 weeks, staying below ~80/week as a buffer. (community-observed, unverified: [ProspectingManual](https://prospectingmanual.com/linkedin-automation/troubleshooting/account-restriction-warnings/))

## Cadence and action budgets

- Connection requests: system-level recommended daily ceiling ~20-30/day; vendor hard caps range from 20-100 requests/day by plan. (vendor-documented: [Dripify](https://dripify.com/features/extra-safety-algorithm/))
- Dripify publishes plan limits (Basic up to 20 requests + 30 messages/day; Pro/Advanced up to 75 requests + 100+ messages/day) and an extra-safe algorithm capped at 100 requests + 150 messages/day. (vendor-documented: [Dripify](https://dripify.com/features/extra-safety-algorithm/))
- Profile views: no official number; observed safe guidance ~80-100 views/day; one vendor blog reports free-account viewing limits around 500/day and premium around 2,000/day and recommends staying under roughly half to avoid scraping flags. (vendor-documented, unverified: [Dripify](https://dripify.com/linkedin-detection-system/); [LeadLoft](https://www.leadloft.com/blog/linkedin-limits))
- Excess profile viewing is itself a restriction trigger, reported to appear without a friendly warning and to block features for days to a week on first offense. (vendor-documented, unverified: [LeadLoft](https://www.leadloft.com/blog/linkedin-limits))
- Pending-invitation ceiling, weekly ceilings, and InMail/DM caps live in [[connection-request-limits]] and [[messaging-limits]]; keep pending under ~400-500 and withdraw stale invites. (cross-reference)
- Treat views + connection requests + messages as ONE combined daily action budget per account, not separate unlimited pipelines. (analysis/inference from vendor daily-limit schemes — flag as inference)

## Humanization mechanics

- Random delays between every action, with varied intervals (seconds to minutes), never a fixed cadence. (vendor-documented: [Dripify](https://dripify.com/features/extra-safety-algorithm/))
- Simulate complete human behavior: mix normal page views, likes, and clicks in with outreach actions rather than only executing outbound steps. (vendor-documented: [Dripify](https://dripify.com/features/extra-safety-algorithm/))
- Keep automation inside realistic working hours; do not appear active 24/7. (vendor-documented: [Dripify](https://dripify.com/linkedin-detection-system/))
- Mix manual and automated activity so the account keeps normal organic usage; personalization protects acceptance, which feeds the safety band in the main note. (vendor-documented: [Dripify](https://dripify.com/linkedin-detection-system/); [Prosp blog](https://www.prosp.ai/blog/linkedin-outreach-without-getting-restricted))

## Infrastructure engineering

- Proxy quality tiers: residential is safest, commercial is in between, datacenter is the most detectable. (vendor-documented: [Dripify](https://dripify.com/linkedin-detection-system/))
- One dedicated, country-matched IP per account is the cross-vendor consensus: Dripify local unique IP (vendor-documented: [Dripify](https://dripify.com/features/extra-safety-algorithm/)); Prosp free per-account proxy from a high-quality provider (vendor-documented: [Prosp help](https://help.prosp.ai/en/articles/10348233-connect-a-linkedin-profile-using-credentials)); HeyReach starter gives each sender a dedicated residential proxy (vendor-documented: [HeyReach pricing](https://www.heyreach.io/pricing/)); Expandi uses country-based residential IPs (vendor-documented: [Expandi](https://expandi.io/blog/linkedin-account-restricted/)).
- LaGrowthMachine adds dedicated IP exclusivity plus mobile (4G) dynamic proxies to appear as a phone user; multiple accounts sharing one IP is the shared-infrastructure pattern Prosp and LGM both warn against. (vendor-documented: [LaGrowthMachine](https://www.lagrowthmachine.com/linkedin-safety/); [Prosp blog](https://www.prosp.ai/blog/linkedin-outreach-without-getting-restricted))
- Never let a tool session and a live browser session on the same account run from different IPs or geo locations at the same time; consistent geo per account. (vendor-documented: [Expandi](https://expandi.io/blog/linkedin-account-restricted/); [Dripify](https://dripify.com/linkedin-detection-system/))
- Prefer cloud-based operation over browser extensions (extensions that modify the UI are detectable; official: [a1341387](https://www.linkedin.com/help/linkedin/answer/a1341387)); after a restriction, clear the browser cache/cookies before manual use. (vendor-documented: [Expandi](https://expandi.io/blog/linkedin-account-restricted/))

## Adaptive safety controls (architecture requirements for our system)

- Per-account adaptive limits that read account health, pending count, acceptance, and past activity: scale up when safe, throttle when strain is detected, and auto-cool-down on sudden spikes or repeated failed actions. (vendor-documented: [Dripify](https://dripify.com/linkedin-detection-system/))
- Enforce hard per-account ceilings at the system level so no campaign can exceed safe bounds; vendors ship this as daily-limit and safe-usage-level enforcement. (vendor-documented: [HeyReach](https://www.heyreach.io/pricing/); [Expandi](https://expandi.io/blog/linkedin-account-restricted/))
- Working-hours scheduling gate for all outbound actions. (vendor-documented: [Dripify](https://dripify.com/linkedin-detection-system/))
- Monitor for warning and verification prompts as friction signals and surface them to the user immediately. (analysis from vendor guidance — flag as inference)

## Restriction response (reactive)

- Official path: disable the automating software; the account auto re-enables at the suspension-notification time; change your password regularly; the exact tool language is in the main note. (official: [Help a1340567](https://www.linkedin.com/help/linkedin/answer/a1340567))
- Practitioner protocol: stop ALL automation immediately, log out of tools, revoke app permissions (Settings > Data Privacy > Other applications), rest 24-72 hours before acting, and do not submit multiple appeals. (community-observed, unverified: [Northlight](https://northlight.ai/blog/linkedin-account-restricted-fix); [Expandi](https://expandi.io/blog/linkedin-account-restricted/))
- Never create a new account while the original is restricted — reported to get both banned; wait about a month before reconnecting automation, and treat a warning as a final strike by slowing all activity for at least a week. (community-observed, unverified: [Northlight](https://northlight.ai/blog/linkedin-account-restricted-fix); [Expandi](https://expandi.io/blog/linkedin-account-restricted/))
- Withdraw stale pending invites in daily batches of 20-30 until under ~500 (mass withdrawal can itself flag); rewrite note templates to cut spam-flag rate by referencing a trigger event, the recipient's role, or specific content. (community-observed, unverified: [ProspectingManual](https://prospectingmanual.com/linkedin-automation/troubleshooting/account-restriction-warnings/))
- Identity/ID verification requests must be handled through LinkedIn's flow, never ignored; they are reported as more serious than a weekly-limit warning. (vendor-documented: [Expandi](https://expandi.io/blog/linkedin-account-restricted/))

## Must-do prevention checklist

- Warm up a new or dormant account 3-4 weeks before any outreach.
- Ramp slowly off the account's own baseline; never spike volume.
- Keep every account inside its daily combined action budget (views + requests + messages).
- Randomize timing and mix organic activity into every automated session.
- Keep automation inside realistic working hours.
- Give each account a dedicated, country-matched residential IP and stable geo.
- Enforce adaptive, per-account safety limits plus hard system ceilings.
- On any warning or verification prompt, pause automation and alert the user.

## Changelog

- 2026-08-12 — Created from Prosp, Dripify, Expandi, LaGrowthMachine, HeyReach docs plus practitioner recovery guides.