
# Engineering Incident Response Policy

**Status:** Synthetic project data
**Department:** Engineering
**Classification:** Restricted internal

## Purpose

This policy describes how the fictional Engineering team at BDACC Technologies identifies, reports, prioritizes, and responds to technical incidents.

The severity levels and response targets below are synthetic values created for testing the TrustRAG knowledge assistant.

## Incident severity levels

### SEV-1 â€” Critical

A critical incident causes a major production outage, significant data unavailability, or a severe disruption to a core company service.

- Acknowledgement target: 15 minutes.
- Notify: Engineering incident lead and Security team.
- Response: Begin immediate investigation and provide regular status updates.

### SEV-2 â€” High

A high-severity incident significantly affects a feature or service, but a workaround may be available.

- Acknowledgement target: 1 hour.
- Notify: Engineering team lead.
- Response: Investigate the cause, document the impact, and implement a suitable resolution.

### SEV-3 â€” Normal

A normal incident affects a limited feature or causes a minor technical issue without a major service disruption.

- Acknowledgement target: 1 business day.
- Notify: The responsible Engineering team.
- Response: Record the issue, investigate it, and schedule corrective work.

## Incident reporting procedure

1. Record a clear description of the incident.
2. Include the affected service, observed symptoms, and approximate start time.
3. Assign a severity level based on the impact.
4. Notify the appropriate responders.
5. Record investigation findings and resolution steps.
6. Document the root cause and preventive actions after resolution.

## Security-related incidents

Suspected unauthorized access, exposed credentials, or unexpected disclosure of sensitive information must be reported to the Security team immediately.

Credentials, access tokens, and other secrets must not be copied into incident reports or ordinary project documentation.

## Review and ownership

The Engineering team maintains this policy in coordination with the Security team. The policy should be reviewed when incident procedures or response targets change.
