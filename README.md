# Space-Track

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
