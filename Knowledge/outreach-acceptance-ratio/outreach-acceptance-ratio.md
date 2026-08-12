---
title: "Outreach Acceptance Ratio as the Volume Gate"
date: 2026-08-12
author: ""
last_audited: 2026-08-12
tags: ["outreach","acceptance-ratio","deliverability","knowledge"]
status: literature
sources:
  - https://www.prosp.ai/blog/linkedin-outreach-without-getting-restricted
  - https://www.linkedin.com/help/linkedin/answer/a551012
references:
  - Research/linkedin-outreach-policy/connection-request-limits
  - Research/linkedin-outreach-policy/ban-prevention-playbook
  - Knowledge/linkedin-platform-detection-model
---

## Summary

In cold social outreach, the practical gate on safe send volume is acceptance
or response ratio, not a fixed cap. When acceptance is low, every unaccepted
request is a negative signal to the platform and volume becomes unsafe; when
acceptance is healthy, more volume can be sent safely. Observed healthy band
is roughly 30-45 percent acceptance, with danger below about 20-30 percent.
First-week response doubles as a fast targeting-feedback signal.

## Notes

- The lever, not the number: low acceptance feeds the platform's official triggers (ignored, pending, spam-marked invitations), so it raises restriction risk independent of volume. (official trigger: [a551012](https://www.linkedin.com/help/linkedin/answer/a551012); lever framing: [Prosp blog](https://www.prosp.ai/blog/linkedin-outreach-without-getting-restricted))
- Healthy band: roughly 30-45 percent acceptance; danger zone below about 20-30 percent. (vendor-documented, unverified: [Prosp blog](https://www.prosp.ai/blog/linkedin-outreach-without-getting-restricted))
- Benchmark data: average acceptance around 37 percent in a large single-platform sample (16,492 invitations, Botdog 2025), with most accepts landing early (63 percent within a day, 88 percent within a week). (vendor-documented, unverified: [Prosp blog](https://www.prosp.ai/blog/linkedin-outreach-without-getting-restricted) citing Botdog)
- Feedback speed: if a batch is still mostly pending after one week, targeting or messaging is the likely problem and should be fixed before it compounds into the pending trigger. (vendor-documented: [Prosp blog](https://www.prosp.ai/blog/linkedin-outreach-without-getting-restricted))
- Consequence for product design: acceptance monitoring is a first-class signal — gate send-rate on observed acceptance and use first-week response to score targeting quality. (analysis/inference from the above — flagged as inference)
- Quality compounds: better targeting raises acceptance, which is what safely unlocks more volume. (vendor-documented: [Prosp blog](https://www.prosp.ai/blog/linkedin-outreach-without-getting-restricted))

## References

Ceiling numbers and pending-invitation guidance live in Research — see
[[Research/linkedin-outreach-policy/connection-request-limits]]. Safety
linkage: [[Research/linkedin-outreach-policy/ban-prevention-playbook]].
Knowledge sibling: [[linkedin-platform-detection-model]].

## Changelog

- 2026-08-12 — Created.