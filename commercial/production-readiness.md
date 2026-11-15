# Production-readiness gate

**Status: NOT PRODUCTION-READY FOR CONFIDENTIAL DEAL DATA.**

This document separates repository quality from operational readiness. A green test suite or successful deployment does not make the current prototype suitable for live transaction documents.

## Current capabilities

- Selectable-text PDF extraction with page and line references.
- Spreadsheet cell-value extraction with sheet and cell references.
- Structured CSV observation import.
- Analyst confirmation before extracted candidates enter the comparison ledger.
- Deterministic value, unit, duplicate-source, missing-value and source-coverage classifications.
- JSON, CSV and standalone HTML exports.
- Synthetic example and public explanation of method and limitations.

## Blocking gaps

| Area | Current position | Required before production |
|---|---|---|
| Identity | No workbench authentication | Strong authentication and account lifecycle |
| Authorisation | No role model | Least-privilege roles and deal-level access |
| Tenant isolation | Not implemented | Verified tenant and deal isolation |
| Confidential files | Public prototype only | Approved private processing boundary |
| Storage | No production retention controls | Encryption, retention, deletion and backup policy |
| Auditability | No immutable event history | Tamper-evident activity and reviewer decisions |
| File safety | Basic file-size check in UI | Server-side limits, parser isolation and resource controls |
| Review governance | Analyst-confirmed inputs | Reviewer sign-off, versioned evidence and change history |
| Operations | No production SLO or incident process | Monitoring, alerting, incident response and recovery tests |
| Assurance | Prototype tests only | Threat model, security review and independent testing |

## Release gates

1. **Product correctness:** regression suite covers classification, extraction boundaries, deterministic exports and adversarial input.
2. **Security architecture:** threat model, data-flow map, identity, authorisation, tenant isolation and secure file processing reviewed.
3. **Data governance:** written data-processing terms, retention/deletion policy, backup controls and incident response approved by the responsible business operator.
4. **Operational readiness:** monitoring, alerting, recovery, dependency scanning and deployment rollback tested.
5. **Professional governance:** qualified finance professionals supervise interpretation; an authorised business representative controls engagements and client-data arrangements.
6. **Deployment verification:** public website, inquiry delivery and workbench are tested in their actual hosting environments using synthetic data.

## Permitted demo posture

Until every relevant gate is met, use synthetic data or properly redacted material with explicit authorisation. Never invite users to upload confidential deal files to the public prototype. Do not claim audit-grade traceability, security certification, validated savings, customer outcomes, or production readiness.
