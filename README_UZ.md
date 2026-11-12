# IELTS Boost — Stage 56 UX, Accessibility & Performance

**Release:** `56.0.0-performance-accessibility`  
**Primary entry:** `index.html`  
**GitHub Pages repository path:** `/final-stage-/`

## Stage 56 highlights

- The initial `data/app-data.json` is 5,938,780 bytes versus 15,201,551 bytes in Stage 55 (**60.93% smaller**).
- The 672 words used by the 84-day core plan remain in the initial payload.
- The full 19,000-word vocabulary remains complete in `data/vocabulary-index.json` and loads only when Vocabulary Lab or a vocabulary-only game needs it.
- Vocabulary search is debounced by 110 ms and normalization is memoized with a bounded cache.
- Service Worker does not precache the 9.6 MB vocabulary index; it caches it on demand.
- Accessibility updates include skip navigation, focus-visible, dynamic accessible names, current-page semantics, reduced-motion and forced-colors styles.
- Responsive browser checks cover 320–1365 CSS pixels.

## Preserved functionality and content

84-day curriculum, all four IELTS skills, 840 Reading questions, 420 Listening questions, 864 sentence patterns, 61 articles, 336 skill-resource records, 84 Listening companions, 84 Task 1 datasets, 84 MP3 files and all 19,000 vocabulary records remain included. Stage 55 backup/restore manager and both IndexedDB audio paths remain in the main app.

`standalone.html` remains byte-identical to the Stage 52 fallback and does not contain Stage 56 lazy-load/accessibility improvements. For Stage 56 functionality, deploy `index.html` with the complete folder tree.

## Deploy

1. Extract `IELTS_Boost_Stage56_UX_Accessibility_Performance.zip`.
2. Upload every ZIP entry to the repository root, not the ZIP file itself.
3. Keep `index.html`, `manifest.webmanifest`, `sw.js`, `assets/`, `data/`, `audio/` and `icons/` in the same root layout.
4. GitHub Settings → Pages → Deploy from a branch → `main` → `/(root)`.
5. Open the HTTPS Pages URL and allow the new shell to load. The full vocabulary index is downloaded only when the Vocabulary Lab is opened.

## Backup

The Stage 55 Full-device Backup & Restore remains available in Settings and Advanced Studio. It can package Main, legacy and Advanced Studio state plus audio blobs from both IndexedDB stores. Store the resulting `.ibbackup.json` privately; it can contain voice recordings.

## QA

See `QA_REPORT_UZ.md`, `docs/STAGE56_MASTER_REPORT_UZ.md`, and machine-readable test reports in `docs/`. Stage 56 automated results: static 65/65, HTTP 109/109, Chromium 65/65 with 2 skipped secure-origin checks, Service Worker simulation 11/11, architecture 8/8, backup regression 14/14.

**Not production accepted yet:** public GitHub Pages, physical Android, mic/ASR, live HTTPS WebCrypto check and actual offline cold-start are reserved for Stage 57. No measured wall-clock performance or WCAG certification is claimed.
