# Project 22: Cron, Services, and Writable Path Misconfigurations

**Level:** Intermediate  
**Environment:** HTB-assigned machine or Academy lab only

## Objective

Review scheduled tasks and service configuration for unsafe ownership or writable execution paths.

## Scope and authorization

Use only the assigned HTB target, domain, and lab credentials. Confirm that every host and account is included in the active exercise scope. No credential theft, password spraying, real-world relay, persistence, or out-of-scope lateral movement.

## Prerequisites and tools

crontab; systemctl; find; ls -l; ps

- Dedicated lab VM and active HTB access.
- Explicit target/domain scope and test identity.
- Evidence directory; redact credentials, hashes, flags, and tokens.

## Procedure

Inspect current-user crontab, /etc/crontab, /etc/cron.* and relevant systemd unit definitions. Check parent-directory and script permissions with namei -l and stat. Identify whether an unprivileged user can alter a file that a privileged process executes. Do not edit or trigger system tasks.

## Expected outcome

A permissions-based finding with execution context, ownership, and safe remediation recommendation.

## Evidence and screenshot checklist

Capture a screenshot of the assigned lab context, a terminal/console view of the relevant read-only enumeration, and a final validation/remediation view. Redact secrets and personal account identifiers. The three images below are simulated diagrams—not actual machine screenshots, command output, or proof of exploitation. Add your own screenshots after running the lab.

## Simulated training illustrations

![Simulated workflow](images/01-workflow.svg)

![Simulated findings](images/02-findings.svg)

![Simulated validation](images/03-validation.svg)

## Findings worksheet

| Field | Evidence to record |
|---|---|
| Affected asset | [Assigned host/domain] |
| Configuration | [Exact permission, policy, or relationship] |
| Proof | [Redacted command output and screenshot] |
| Security impact | [Privilege, confidentiality, integrity, availability] |
| Severity | [Rating and rationale] |
| Confidence | [Confirmed / likely / unconfirmed] |

## Defensive interpretation and remediation

Recommend least privilege, managed identities, secure service configuration, modern authentication, appropriate SMB signing and protocol policy, strong unique secrets, and monitoring as relevant. Map confirmed conditions to CWE or applicable Microsoft security guidance. Do not infer exploitability from enumeration alone.

## Retest

Repeat the same read-only query after the configuration change. Confirm the risky permission, relationship, or policy is corrected and document any residual exposure.

## Deliverables

- Scope and tool/version record.
- Three redacted screenshots from your own lab run.
- Sanitized evidence and confirmed risk analysis.
- Remediation and retest notes.

## References

- [Hack The Box](https://www.hackthebox.com/)
- [HTB Academy](https://academy.hackthebox.com/)
- [Impacket](https://github.com/fortra/impacket)
- [BloodHound](https://bloodhound.specterops.io/)
