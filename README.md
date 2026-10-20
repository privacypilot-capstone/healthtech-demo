# healthtech-demo

# HealthTrack India — PrivacyPilot Synthetic Benchmark

This repository is a synthetic health-application codebase used to
evaluate PrivacyPilot's detection of potential privacy-policy and
personal-data-handling issues.

## Evaluation scope

The benchmark supports evaluation of potential issues related to:

- Section 5 — Notice
- Section 6(1) — Consent
- Section 8(2) — Data fiduciary responsibility in processor arrangements
- Section 8(5) — Reasonable security safeguards
- Rule 3(b) — Notice requirements

## Evaluation principles

- Compare personal-data processing in executable code with the privacy policy.
- Distinguish actual data flows from comments and documentation.
- Treat potential data-minimisation concerns as review signals, not
  automatically as proven legal violations.
- Do not infer missing consent or missing processor contracts from code alone.
- Do not treat the presence of a logging or external-service call alone
  as proof of a security-safeguard violation.
- Record evidence locations and the rationale for each finding.

## Benchmark methodology

Maintain a separate ground-truth manifest containing the expected
findings, non-findings, evidence locations, and applicable provision.
Do not use source-code comments as the ground-truth labels.

Evaluate precision, recall, and F1 against the reviewed manifest.
