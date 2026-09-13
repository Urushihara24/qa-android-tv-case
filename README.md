# Android TV Slideshow App Testing

> Manual QA case covering slideshow playback, caching, offline USB mode, collections, scheduled streams, and behavior differences between online and offline execution.

<p align="center">
  <img src="https://img.shields.io/badge/Android_TV-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android TV">
  <img src="https://img.shields.io/badge/Manual_QA-Testing-6E40C9?style=for-the-badge" alt="Manual QA">
  <img src="https://img.shields.io/badge/Offline-USB_Testing-555555?style=for-the-badge" alt="Offline USB testing">
</p>

| Scope | Evidence | QA focus |
|---|---|---|
| Android TV playback · cache · USB · collections · scheduled streams | Executed test cases · scenario-based bug reports · video references | Expected vs Actual · offline/online comparison · defect isolation |

**Start here:** [test report](docs/REPORT.md) · [test cases](test_cases/TEST_CASES.md) · [bug reports](bugs/BUG_REPORT.md) · [status legend](docs/LEGEND.md)

## What is inside

- `docs/REPORT.md` — report with scenario results (`OK` / `FAIL` / `NOTE`), conclusions, and recommendations.
- `test_cases/TEST_CASES.md` — executed checks; each failed case references the related bug ID.
- `bugs/BUG_REPORT.md` — scenario-based defect reports with steps, Actual, Expected, Severity, and Priority.
- `docs/IMPROVEMENTS.md` — improvement suggestions that are intentionally separated from defects.
- `docs/LEGEND.md` — status and severity legend used across the case.

## How the case is structured

Test cases and defects are linked by ID: the test-case table shows which execution produced each defect, while the bug report explains what failed and what the expected behavior was.

Online and offline behavior were compared deliberately so cache / USB-reading failures could be separated from defects in slideshow content itself. Scenario-specific bugs are kept separate so the supporting video or artifact can be mapped to one concrete failure rather than to a whole testing session.

## QA approach

- execute the scenario and record the observed state;
- compare online and offline behavior when the same content is available through both paths;
- link every failed case to a concrete defect;
- keep product improvements separate from bugs;
- preserve raw runtime wording and evidence references where they matter for reproduction.
