# Project 19: Command Injection and Safe Proof of Execution

**Level:** Intermediate  
**Environment:** HTB-assigned machine or Academy lab only

## Objective

Identify unsafe server-side command construction using non-destructive proof markers in an HTB lab.

## Scope and authorization

Use only your assigned HTB target or an explicitly authorized retired-machine replica. Record target identity, assigned IP, time window, and platform rules. Do not test unrelated systems.

## Prerequisites and tools

Burp Suite; curl; browser

- Dedicated Kali or Windows lab VM as appropriate.
- Active HTB lab access and confirmed scope.
- Evidence folder; keep secrets and flags out of public commits.

## Procedure

Locate a lab parameter that appears to invoke a system utility. Use a harmless arithmetic or fixed-string marker approved by the lab and observe only the expected response delta. Do not spawn shells, write files, establish callbacks, or access host data.

## Expected outcome

Minimal proof that input reaches a command interpreter, with the exact parameter and safe output marker.

## Screenshot and evidence checklist

Capture (1) the HTB lab context with account details obscured, (2) the relevant terminal/Burp output, and (3) manual verification or remediation evidence. The illustrations below are simulated training diagrams, not actual HTB screenshots or proof of execution. Add your own redacted screenshots after completing the exercise.

## Simulated training illustrations

![Simulated workflow](images/01-workflow.svg)

![Simulated findings](images/02-findings.svg)

![Simulated validation](images/03-validation.svg)

## Findings template

| Item | Record |
|---|---|
| Asset / service | [Assigned HTB target] |
| Observation | [What was directly observed] |
| Evidence | [Redacted screenshot and output filename] |
| Impact | [Confidentiality / integrity / availability] |
| Severity | [Rating and rationale] |
| Confidence | [Confirmed / likely / unconfirmed] |

## Remediation

Recommend least privilege, secure defaults, input validation, patching, segmentation, and logging as applicable to the confirmed root cause. Map to a relevant CWE or OWASP category where appropriate. Do not recommend fixes for unverified scanner output.

## Retest

Repeat the smallest safe test after remediation and record before/after behavior, timestamp, and remaining limitations.

## Deliverables

- Scope and methodology notes.
- Three redacted screenshots from your own lab execution.
- Reproducible finding, impact, severity rationale, and remediation.
- Retest result and sanitized command output.

## References

- [Hack The Box](https://www.hackthebox.com/)
- [HTB Academy](https://academy.hackthebox.com/)
