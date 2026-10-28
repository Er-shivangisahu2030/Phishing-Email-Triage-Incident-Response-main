# Phishing Email Triage & Incident Response Workflow

A practical cybersecurity project demonstrating a structured workflow for investigating suspicious phishing emails, extracting Indicators of Compromise (IoCs), performing threat-intelligence analysis, and documenting incident-response actions.

## Project Objective

The project demonstrates a SOC-style workflow for triaging a suspicious email from initial acquisition through threat classification and incident response.

## Investigation Workflow

1. Email acquisition and preservation
2. Email metadata and content analysis
3. IoC extraction
4. File hashing
5. Threat-intelligence assessment
6. Threat classification
7. Incident containment and response
8. Incident documentation

## Case Investigated

**Subject:** DIRECT DEPOSIT CHANGE

**Sender:** shivangi071@gmail.com

**Sender Domain:** gmail.com

**Classification:** Suspected Payroll Fraud / Business Email Compromise (BEC)

**Severity:** HIGH

## Evidence

The investigated email is preserved as:

emails/suspicious_email.eml`n
**SHA-256:**

CD577024C35E474396E261720F813E63CE01E1C1342F30E9DCCF7AF7DC66E703`n
## Indicators of Compromise

| Indicator | Type |
|---|---|
| shivi8f67@gmail.com | Email address |
| stem2mars.com | Domain |
| CD577024C35E474396E261720F813E63CE01E1C1342F30E9DCCF7AF7DC66E703 | SHA-256 |

## Authentication Analysis

The supplied email does not contain Authentication-Results, Received-SPF, or DKIM-Signature headers.

Therefore SPF, DKIM, and DMARC results cannot be determined from this sample.

No authentication results have been fabricated.

## Threat Assessment

The email requests a change to direct-deposit information before payroll processing. This is consistent with characteristics of payroll-fraud phishing because the requested action could redirect an employee's salary to an unauthorized account.

The sender domain is treated as suspicious in the context of this message. Suspicion alone is not considered proof that the infrastructure is malicious.

## Incident Response

Recommended actions include:

- Do not process the requested payment change.
- Preserve the original email as evidence.
- Search for related messages from the sender and domain.
- Identify potentially affected recipients.
- Verify financial changes through an independent communication channel.
- Block confirmed malicious indicators after validation.
- Investigate whether any recipient interacted with the email.

## Repository Structure

```text
Phishing-Email-Triage-Incident-Response/
├── emails/
│   └── suspicious_email.eml
├── analysis/
│   ├── email_analysis.md
│   └── threat_intelligence.md
├── iocs/
│   └── ioc_list.csv
├── architecture/
│   └── phishing_email_triage_workflow.png
├── docs/
│   └── incident_response_report.md
├── .gitignore
└── README.md
```

## Tools

- PowerShell
- VirusTotal
- URLScan.io
- MXToolbox
- Git / GitHub

## Disclaimer

This project uses a sample phishing email for defensive cybersecurity analysis. The investigation focuses on evidence preservation, threat assessment, IoC identification, and incident response.
