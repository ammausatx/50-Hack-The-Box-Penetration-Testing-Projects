# Project 30: Metasploit Auxiliary Scanning and Module Selection

**Level:** Intermediate  
**Environment:** HTB-assigned machine or Academy lab only

## Objective

Use Metasploit auxiliary modules for narrowly scoped service verification on an HTB target.

## Scope and authorization

Use only the assigned HTB target, domain, and lab credentials. Confirm that every host and account is included in the active exercise scope. No credential theft, password spraying, real-world relay, persistence, or out-of-scope lateral movement.

## Prerequisites and tools

Metasploit Framework; Nmap; assigned HTB target

- Dedicated lab VM and active HTB access.
- Explicit target/domain scope and test identity.
- Evidence directory; redact credentials, hashes, flags, and tokens.

## Procedure

Search modules by service and inspect module documentation before use. Set RHOSTS to the single assigned target and required RPORT explicitly. Prefer scanner or version-check modules; run one module at a time with conservative options and save sanitized output.

## Expected outcome

A rationale for module selection, configured scope, observed result, and independent corroboration.

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
