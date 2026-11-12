# IELTS Boost Stage 56.0 — QA Report

Release: `56.0.0-performance-accessibility`

## Results

| Test suite | Pass | Fail | Skipped |
|---|---:|---:|---:|
| Static QA | 65 | 0 | 0 |
| Local HTTP subpath smoke | 109 | 0 | 0 |
| Chromium DOM runtime | 65 | 0 | 2 |
| Service Worker simulation | 11 | 0 | 0 |
| Architecture contract | 8 | 0 | 0 |
| Backup regression | 14 | 0 | 0 |

**Two browser checks skipped:** native secure-context/WebCrypto and live HTTPS. The browser harness uses an opaque origin because managed browser policy blocks public HTTPS navigation. The app-data and vocabulary asset SHA-256 values are verified by Python static QA.

## Commands

```bash
python tests/run_static_qa_56.py
python tests/run_http_smoke_56.py
python tests/run_browser_acceptance_56.py
node tests/run_service_worker_sim_56.js
node tests/run_architecture_contract_56.js
node tests/run_backup_manager_tests_56.js
```

## Content and integrity

- Main app-data payload: 5,938,780 bytes; Stage55 baseline: 15,201,551 bytes; reduction: 60.93%.
- Full 19K vocabulary index: 9,627,303 bytes; 19,000 unique IDs; 672 daily core words retained.
- Standalone fallback SHA-256: `1527dccc51e2fec26ea2b30e711000b69236e4d3f28cf7c907ee7929b37c4425` (unchanged from Stage 52).
- Stage 55 rollback archive SHA-256: `c2849db7a11dc35c05ca1ba6b5a279fd60f2269f16b0ff362d2b4119a883245a` (unchanged).

See `docs/STAGE56_MASTER_REPORT_UZ.md` and the machine-readable test reports in `docs/`.

## Not tested
Public Pages deployment/acceptance, physical Android, microphone and native ASR, native secure HTTPS digest execution and actual Service Worker offline cold-start. Automated accessibility checks do not constitute WCAG certification.
