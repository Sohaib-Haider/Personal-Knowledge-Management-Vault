---
title: "LinkedIn Automation Policy & Send Limits"
date: 2026-08-09
author: ""
last_audited: 2026-08-09
tags: ["linkedin","research","compliance","outreach","policy"]
status: completed
sources:
  - https://www.linkedin.com/legal/user-agreement
  - https://www.linkedin.com/help/linkedin/answer/a550555
  - https://www.linkedin.com/help/linkedin/answer/a551012
  - https://www.linkedin.com/help/linkedin/answer/a1341387
  - https://www.linkedin.com/help/linkedin/answer/a1340567
  - https://www.linkedin.com/legal/crawling-terms
  - https://www.linkedin.com/help/linkedin/answer/a543695/inmail-message-credits-and-renewal-process
  - https://www.linkedin.com/help/sales-navigator/answer/a101030
  - https://taplio.com/blog/linkedin-connection-request-limit
  - https://we-connect.io/blog/linkedin-limits-2026-complete-guide
  - https://linkedapi.io/guides/linkedin-connection-limit-2026
  - https://phantombuster.com/blog/linkedin-automation/linkedin-limit-reset-schedule/
references: ["Ideas/linkedin-outreach-assistant"]
---

## Question

What does LinkedIn's policy actually say about third-party automation, and
what limits constrain sending connection requests and messages (official or
community-observed)?

## Hypothesis

Expected the User Agreement to broadly bar bots, scraping, and automated
message sending; expected LinkedIn to publish NO official numeric send caps
(limits described but never quantified); and expected community practitioner
sources to be the only practical source of numeric thresholds. Expected
Premium/InMail credits to be the one area with official published numbers.

## Log / Findings

- 2026-08-09 — Started.

### Official: policy prohibits automation

- UA 8.2(2): no software, scripts, robots, crawlers, plugins or any means to scrape or copy the Services. (official: [LinkedIn User Agreement](https://www.linkedin.com/legal/user-agreement))
- UA 8.2(13): no bots or unauthorized automated methods to access the Services, "add or download contacts, send or redirect messages", or create/comment/like/share posts. (official: [LinkedIn User Agreement](https://www.linkedin.com/legal/user-agreement))
- UA 8.2(15): no overlaying or modifying the Services' appearance (browser-extension overlays). (official)
- UA 3.4: LinkedIn may limit your connections and ability to contact members; may restrict/suspend for misuse. (official)
- UA 3.6: generative AI writing features exist, but generated content must be reviewed/edited and comply with policies. (official)
- Help a1341387: third-party software/crawlers/bots/plugins that scrape, modify, or automate violate the UA; risk of restriction or shutdown; tools may stop working without notice. (official)
- Help a1340567: accounts restricted for automated activity; disabling the software auto-re-enables at the time in the suspension notice. (official)
- Crawling Terms: Automated Crawling & Indexing without express permission of LinkedIn is strictly prohibited. (official: [crawling-terms](https://www.linkedin.com/legal/crawling-terms))

### Official: send limits exist, no numbers published

- Help a550555: invitation limits apply to ALL members (Basic and Premium); reaching them triggers a temporary restriction "typically" lasting one week; withdrawing pending invitations does NOT remove it; you cannot buy more invitations; LinkedIn cannot shorten the wait; Support cannot disclose the reason. (official: [LinkedIn Help a550555](https://www.linkedin.com/help/linkedin/answer/a550555))
- Help a550555: Basic members may add a personalized note to 5 connection requests per month; Premium members can send unlimited personalized notes. (official: [LinkedIn Help a550555](https://www.linkedin.com/help/linkedin/answer/a550555))
- Help a551012: triggers are excessive invites in a short time, many invitations ignored/pending/marked spam, and automation-tool suspicion with excessive sending (may suspend/restrict). (official: [LinkedIn Help a551012](https://www.linkedin.com/help/linkedin/answer/a551012))
- Help a551012: max 30,000 1st-degree connections; no re-invite to the same recipient for up to 3 weeks after withdrawal; standard vs personalized invites have separate limits; most restrictions auto-remove within one week; repeated suspensions may become permanent. (official: [LinkedIn Help a551012](https://www.linkedin.com/help/linkedin/answer/a551012))
- Help a551012: first restriction → wait a few hours; multiple in a day → wait a few days; too many outstanding → wait up to one month. (official: [LinkedIn Help a551012](https://www.linkedin.com/help/linkedin/answer/a551012))
- Observation recorded honestly: the Help pages confirm limits exist but provide NO numeric weekly or daily caps. (official: [LinkedIn Help a550555](https://www.linkedin.com/help/linkedin/answer/a550555), [LinkedIn Help a551012](https://www.linkedin.com/help/linkedin/answer/a551012))

### Official: InMail / messaging numbers

- Help a543695: monthly InMail credits — Premium Career 5, Premium Business 15, Sales Navigator Core 50, Recruiter Lite 30. (official: [LinkedIn Help a543695](https://www.linkedin.com/help/linkedin/answer/a543695/inmail-message-credits-and-renewal-process))
- Help a543695: max accumulation — Career 15, Business 45, SN 150, Recruiter Lite 120; no unlimited-InMail plan; credit refunded if accepted/declined/responded within 90 days; no new InMail to a member until they respond. (official: [LinkedIn Help a543695](https://www.linkedin.com/help/linkedin/answer/a543695/inmail-message-credits-and-renewal-process))
- Sales Navigator help a101030: all SN tiers 50/month, accumulate to 150, usable within 90 days; extra credits cannot be purchased; responses refund a credit. (official: [LinkedIn Help Sales Navigator a101030](https://www.linkedin.com/help/sales-navigator/answer/a101030))

### Community-observed (UNVERIFIED — not official facts)

- Sub-notes hold the detail: [[connection-request-limits]] and [[messaging-limits]].
- Consensus across Taplio, We-Connect, LinkedAPI, PhantomBuster: no official fixed number; "around 100/week" baseline; rolling 7-day reset (not calendar); new accounts ~50-80/week; trusted accounts up to ~200/week; safe daily pacing — see connection-request-limits.md for tiered daily pacing; pending-invitation guidance: keep under ~400-500; restrictions commonly reported around ~700; warnings above ~1,500. (community-observed, unverified: [Taplio blog](https://taplio.com/blog/linkedin-connection-request-limit); [We-Connect blog](https://we-connect.io/blog/linkedin-limits-2026-complete-guide); [LinkedAPI](https://linkedapi.io/guides/linkedin-connection-limit-2026); [PhantomBuster blog](https://phantombuster.com/blog/linkedin-automation/linkedin-limit-reset-schedule/))

### Hypothesis vs outcome

Confirmed: UA broadly bars bots/automation and automated message sending
(verified). Confirmed: no official numeric weekly caps — Help pages describe
limits without numbers. Confirmed: Premium/InMail credits are the only area with
official published numbers. Community thresholds remain the practical source of
send-limit guidance — flagged UNVERIFIED throughout. (outcome of this research)

## Sources

Official (all fetched live 2026-08-09):
- LinkedIn User Agreement — https://www.linkedin.com/legal/user-agreement
- Invitation limit reached — https://www.linkedin.com/help/linkedin/answer/a550555
- Types of restrictions for sending invitations — https://www.linkedin.com/help/linkedin/answer/a551012
- Prohibited software and extensions — https://www.linkedin.com/help/linkedin/answer/a1341387
- Automated activity on LinkedIn — https://www.linkedin.com/help/linkedin/answer/a1340567
- LinkedIn Crawling Terms and Conditions — https://www.linkedin.com/legal/crawling-terms
- InMail message credits and renewal process — https://www.linkedin.com/help/linkedin/answer/a543695/inmail-message-credits-and-renewal-process
- Understand InMail credits in Sales Navigator — https://www.linkedin.com/help/sales-navigator/answer/a101030

Community (all fetched live 2026-08-09, UNVERIFIED):
- Taplio blog — https://taplio.com/blog/linkedin-connection-request-limit
- We-Connect blog — https://we-connect.io/blog/linkedin-limits-2026-complete-guide
- LinkedAPI guide — https://linkedapi.io/guides/linkedin-connection-limit-2026
- PhantomBuster blog — https://phantombuster.com/blog/linkedin-automation/linkedin-limit-reset-schedule/

## Changelog

- 2026-08-09 — Created.
- 2026-08-09 — Initial live research complete.
- 2026-08-09 — Completed: official policy verified against live sources; community thresholds labeled unverified.
- 2026-08-09 — Inline official source URLs added.