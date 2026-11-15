# Security policy

## Current security boundary

DealTie is a prototype analyst workbench. It is **not approved for confidential transaction material, personal financial information, or production deal-room use**. Do not upload confidential CIMs, QoE reports, valuation models, customer records, credentials, or other sensitive material to a public deployment.

The current workbench does not provide user authentication, tenant isolation, role-based access, encryption-at-rest guarantees, managed retention/deletion, immutable audit history, multi-user access controls, or a security-reviewed confidential-document processing boundary.

## Reporting a vulnerability

Do not publish exploit details, credentials, private documents, or personal data in a public issue. Use GitHub's private vulnerability reporting feature if enabled for this repository. If it is unavailable, contact the repository owner through an independently verified channel and share only the minimum information needed to reproduce the issue.

Include:
- affected commit or deployed version;
- affected component and deployment type;
- concise reproduction steps using synthetic data;
- expected and observed behaviour;
- potential impact and any known mitigations.

Do not test against systems or data you do not own or have explicit permission to assess.

## Release requirements before confidential-data use

A production release requires, at minimum:
- a documented threat model and data-flow inventory;
- authentication, authorisation and tenant isolation;
- encryption in transit and at rest with managed key controls;
- explicit retention, deletion, backup and incident-response procedures;
- upload size, decompression, parser and resource-exhaustion controls;
- dependency and container vulnerability scanning;
- security tests for file parsing, exports, HTML escaping and inquiry endpoints;
- independent review of the deployment and operational controls.

Passing the repository test suite does not satisfy these requirements.
