# Jira Service Management - Tier 1 Ticket Simulation

This repository documents a simulated Tier 1 help desk environment built in Jira Service Management. Five support tickets were created and resolved across two issue types - Service Requests and Incidents - covering the most common categories of end-user IT issues encountered at the help desk level.

The goal was to demonstrate familiarity with the full ticket lifecycle: intake, triage, root cause identification, resolution documentation, and closure.

## Project Setup

Platform: Jira Service Management  
Project name: SOC Lab IT Support Desk  
Project type: IT Service Management  
Ticket types used: Service Request, Incident

## Tickets

Each ticket was written from the perspective of a non-technical end user submitting a request.  
Resolution comments were written from an analyst perspective, documenting triage steps, root cause, and resolution actions as they would appear in a real ticketing environment.

| # | Summary | Type | Priority | Root Cause |
| - | ------- | ---- | -------- | ---------- |
| 1 | I can't log into my computer - it says my account is locked | Service Request | High | AD lockout triggered by stale credentials on secondary device |
| 2 | My VPN keeps disconnecting every few minutes | Incident | Medium | NTP drift causing periodic certificate validation failure |
| 3 | I can't access the shared drive - it was working yesterday | Incident | Medium | GPO refresh failure - drive mapping policy not applied on last login |
| 4 | My MFA app isn't generating codes and I'm locked out | Service Request | High | TOTP drift caused by manually set device clock |
| 5 | Printer on the second floor stopped working for everyone | Incident | Low | Print spooler crash on print server following Windows update |

---

# Resolution Documentation Approach

Each resolution comment follows the same structure:
- Initial triage - what the user reported and what was verified first
- Root cause identification - what was actually causing the issue, not just the symptom
- Resolution steps - exactly what was done to fix it
- User advisement - what the user was told to prevent recurrence
- Escalation decision - whether the ticket warranted escalation and why

Standard documentation practice providing real value to any other analyst working with the ticket. Comments in this simulation are written to stand on their own. Anyone reading after closure should be able to understand exactly what happened and why.

# Ticket Selection Rationale

These five tickets represent the most frequently recurring issue categories at the Tier 1 and Tier 2 help desk level:
- **Account lockout** - one of the highest-volume ticket types in any environment with Active Directory
- **VPN connectivity** - the dominant remote work support issue, with multiple possible root causes that require methodical triage
- **Drive mapping failure** - a GPO-dependent issue that looks like a permissions problem on the surface, but often isn't
- **MFA failure** - increasingly common as MFA becomes enforced across all systems; time sync is a non-obvious root cause most users fail to identify themselves
- **Print server failure** - a server-side issue that presents as an individual user problem, requiring an analyst to recognize wide impact and shift the investigation scope accordingly

# Screenshots

All found in the [screenshots](./screenshots) directory.
