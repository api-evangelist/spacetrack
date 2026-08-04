# Space-Track

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Space-Track.org is the official US military space surveillance REST API operated by the 18th Space Control Squadron of the US Space Force. It provides unclassified space situational awareness data including Two-Line Element (TLE) sets, conjunction data messages (CDMs), satellite catalog information, decay and reentry predictions, and tracking and impact predictions for all Earth-orbiting objects tracked by the US Space Surveillance Network.

## Overview

- **Base URL:** https://www.space-track.org
- **API Type:** REST
- **Authentication:** Session cookie (username/password login)
- **Cost:** Free (US Government policy; registration required)
- **Operator:** 18th Space Control Squadron, US Space Force

## Key API Classes

| Class | Controller | Description |
|-------|-----------|-------------|
| gp | basicspacedata | Current General Perturbations (SGP4 element sets / TLEs) |
| gp_history | basicspacedata | 138+ million historical orbital element sets |
| satcat | basicspacedata | Satellite catalog with metadata for all tracked objects |
| cdm_public | basicspacedata | Public conjunction data messages |
| tip | basicspacedata | Tracking and Impact Prediction (reentry) messages |
| decay | basicspacedata | Satellite reentry predictions and history |
| boxscore | basicspacedata | Summary statistics on tracked objects |
| cdm | expandedspacedata | Full conjunction data messages (approved users) |
| maneuver | expandedspacedata | Maneuver data for cooperative satellites |

## Data Formats

- JSON
- CSV
- XML (OMM)
- KVN
- TLE (two-line element)
- 3LE (three-line element)
- HTML

## Rate Limits

- 30 requests per minute (global)
- 300 requests per hour (global)
- Per-class limits apply (e.g., GP: 1/hour, SATCAT: 1/day)

## Links

- [Portal](https://www.space-track.org)
- [Documentation](https://www.space-track.org/documentation)
- [Register](https://www.space-track.org/auth/createAccount)
- [Contact](https://www.space-track.org/contactus/)
