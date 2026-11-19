# Project 09: HTTP Virtual Host Enumeration

**Level:** Beginner  
**Environment:** HTB-assigned machine or Academy lab only  
**Status:** Training guide — add your own results after completing the exercise.

## Objective

Identify name-based virtual hosts only within hostnames and addresses assigned by HTB.

## Scope and authorization

Use only the target IP/hostname assigned to your active HTB lab or an explicitly authorized retired-machine environment. Record machine name, assigned address, start/end time, and HTB rules before testing. Never substitute a public IP or unrelated host.

## Prerequisites and tools

ffuf; curl; known HTB hostname or lab domain

- Kali Linux or a dedicated testing VM.
- Active HTB VPN or official browser-based lab environment.
- Create an evidence/ directory for notes and command output.
- Confirmed target identifier and explicit scope.

## Lab procedure

Use the machine-provided hostname and target IP. Add the assigned hostname to a temporary hosts entry only if required. Compare the default response with a small candidate list using ffuf -u http://TARGET/ -H Host:FUZZ.htb -w evidence/host-candidates.txt -rate 10 -fs BASELINE_SIZE. Replace placeholders with lab values and manually inspect differences.

## Expected observations

Record candidate hostnames, response fingerprints, and confirmation via the assigned lab hostname. Exclude random internet DNS lookups.

## Evidence to capture

1. Screenshot of the HTB machine/lab context with sensitive account details hidden.
2. Terminal or Burp screenshot showing the command/request and relevant output, with tokens, flags, and credentials redacted.
3. Screenshot or note showing manual validation and final conclusion.

The three diagrams below are simulated explanatory visuals. They are not genuine screenshots or claims that a target was tested. Add your own redacted screenshots when you perform the lab.

## Simulated training illustrations

![Simulated workflow illustration](images/01-workflow.svg)

![Simulated findings illustration](images/02-findings.svg)

![Simulated validation illustration](images/03-validation.svg)

## Findings and risk assessment

| Field | Your evidence |
|---|---|
| Finding | [Confirmed issue, or state none found] |
| Affected asset | [HTB machine and in-scope service] |
| Evidence | [Screenshot filename, command, response excerpt] |
| Impact | [Confidentiality, integrity, availability] |
| Severity | [Informational / Low / Medium / High / Critical, with rationale] |
| Confidence | [Confirmed / Likely / Unconfirmed] |

Do not claim a vulnerability based only on a scanner banner or an unverified hypothesis.

## Remediation guidance

Do not enumerate unrelated domains or use third-party DNS brute-force services. Keep all host-header requests directed to the assigned HTB IP.

Map confirmed weaknesses to applicable CWE or OWASP categories, explain root cause, recommend least-privilege fixes, and identify a safe retest.

## Validation and retest

Repeat the minimal test after remediation. Record before/after behavior, tool versions, timestamps, and limitations. Demonstrate that the original condition is no longer reproducible without introducing new risk.

## Deliverables

- Scope and methodology notes.
- Sanitized command output and three redacted evidence screenshots from your own lab run.
- Confirmed findings with impact and severity rationale.
- Remediation and retest result.

## References

- [Hack The Box](https://www.hackthebox.com/)
- [HTB Academy](https://academy.hackthebox.com/)
- [Nmap Reference Guide](https://nmap.org/book/man.html)
