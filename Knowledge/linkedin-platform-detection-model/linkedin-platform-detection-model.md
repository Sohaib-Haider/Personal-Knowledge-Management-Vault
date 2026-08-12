---
title: "LinkedIn Platform Detection Model"
date: 2026-08-12
author: ""
last_audited: 2026-08-12
tags: ["linkedin","knowledge","detection","automation","platform-risk"]
status: literature
sources:
  - https://www.linkedin.com/help/linkedin/answer/a550555
  - https://www.linkedin.com/help/linkedin/answer/a551012
  - https://www.linkedin.com/help/linkedin/answer/a1341387
  - https://www.linkedin.com/help/linkedin/answer/a1340567
  - https://www.prosp.ai/blog/linkedin-outreach-without-getting-restricted
  - https://dripify.com/linkedin-detection-system/
  - https://expandi.io/blog/linkedin-account-restricted/
  - https://www.lagrowthmachine.com/linkedin-safety/
references:
  - Research/linkedin-outreach-policy/linkedin-outreach-policy
  - Research/linkedin-outreach-policy/ban-prevention-playbook
  - Ideas/linkedin-outreach-assistant
---

## Summary

LinkedIn governs against automation and scraping with heuristics, not published
rules. It publishes no numeric sending caps; its limits are dynamic and
account-specific. Detection is driven by two complementary signal families
(technical or infrastructure, and behavioral or pattern), plus two operative
levers: deviation from an account's own baseline and acceptance ratio.
Enforcement spans both account-level behavior and infrastructure-level
footprints. Any number practitioners quote is consensus, never policy.

## Notes

- No published numbers: LinkedIn Help states limits exist to prevent misuse but publishes no numeric weekly or daily caps; limits are dynamic and account-specific. (official: [a550555](https://www.linkedin.com/help/linkedin/answer/a550555), [a551012](https://www.linkedin.com/help/linkedin/answer/a551012))
- Official invitation-restriction triggers: sending many invites in a short time; invitations ignored, left pending, or marked spam; suspected automation with excessive sending. (official: [a551012](https://www.linkedin.com/help/linkedin/answer/a551012))
- Technical signals used for detection: datacenter IPs; geographic or IP mismatch; multiple simultaneous logins from different IPs; rotating IPs; browser extensions that modify the page; traffic from servers unrecognized as the user's device. (vendor-documented: [Dripify](https://dripify.com/linkedin-detection-system/))
- Behavioral signals: fixed-cadence or bot-speed actions; identical templated messages at scale; automation running while the user is offline or asleep; sudden spikes off baseline; messaging immediately after connecting; bulk endorsing or following. (vendor-documented: [Dripify](https://dripify.com/linkedin-detection-system/); [Expandi](https://expandi.io/blog/linkedin-account-restricted/))
- Baseline-deviation principle: a sharp jump off an account's own quiet pattern flags it even when the absolute volume is low; the shape of the change, not the count, is the signal. (vendor-documented: [Prosp blog](https://www.prosp.ai/blog/linkedin-outreach-without-getting-restricted))
- Acceptance-ratio principle: ignored, pending, and spam-marked invites are official triggers, so low acceptance feeds them regardless of volume; healthy band observed around 30-45 percent, danger below about 20-30 percent. (official trigger [a551012](https://www.linkedin.com/help/linkedin/answer/a551012); band is vendor-observed, unverified)
- Infrastructure enforcement: multiple accounts sharing one IP reads as an automation service, and 2025 enforcement targeted automation services themselves, not only individual senders. (vendor-documented: [Prosp blog](https://www.prosp.ai/blog/linkedin-outreach-without-getting-restricted); [LaGrowthMachine](https://www.lagrowthmachine.com/linkedin-safety/))
- Restriction durations: typically about one week; up to a month when too many invitations stay pending; automation violations can be permanent. (official: [a550555](https://www.linkedin.com/help/linkedin/answer/a550555), [a551012](https://www.linkedin.com/help/linkedin/answer/a551012))

## References

Operational figures and vendor detail live in Research, never here — see
[[Research/linkedin-outreach-policy/linkedin-outreach-policy]] and
[[Research/linkedin-outreach-policy/ban-prevention-playbook]]. Knowledge
siblings: [[automation-infrastructure-isolation]],
[[platform-restriction-lifecycle]], [[outreach-acceptance-ratio]].

## Changelog

- 2026-08-12 — Created.