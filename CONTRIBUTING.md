# Contributing

DealTie is a narrow, deterministic financial-observation comparison prototype. Contributions should improve traceability, reproducibility, usability, or safety without implying accounting judgement or assurance.

## Development setup

```bash
python -m venv .venv
# Windows: .venv\\Scripts\\activate
# macOS / Linux: source .venv/bin/activate
python -m pip install -r dealtie/requirements.txt
```

## Required checks

```bash
PYTHONPATH=. python -m unittest discover -s dealtie/tests -v
python -m compileall -q dealtie
```

The same checks run in GitHub Actions on pushes and pull requests.

## Engineering rules

- Keep comparison rules deterministic and explicit.
- Never infer currency, scale, period equivalence, source hierarchy, or the correct reported figure.
- Preserve source references and the original analyst-supplied observations.
- Treat malformed or incomplete evidence as a visible exception; do not silently repair it.
- Escape user-controlled text in generated HTML.
- Add regression tests for every change to classification, parsing, or export behaviour.
- Use synthetic fixtures in tests. Never commit client documents, deal data, credentials, or private inquiry details.
- Do not describe a mismatch as an error, loss, recovery, or misstatement without independent professional determination.

## Scope

This repository does not currently implement secure deal-room hosting, authentication, multi-tenant controls, OCR, semantic matching, formula evaluation, currency conversion, or accounting analysis. Do not present unimplemented capabilities as available.
