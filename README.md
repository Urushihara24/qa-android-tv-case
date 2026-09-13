# Android TV Slideshow App Testing

A real-world QA case: manual testing of a client application for Android TV, covering slideshows, caching, offline USB playback, collections, and scheduled streams.  
Author: Vsevolod.

<p align="center">
  <img src="https://img.shields.io/badge/Android_TV-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android TV">
  <img src="https://img.shields.io/badge/Manual_QA-Testing-6E40C9?style=for-the-badge" alt="Manual QA">
  <img src="https://img.shields.io/badge/Offline-USB_Testing-555555?style=for-the-badge" alt="Offline USB testing">
</p>

## What is inside
- `docs/REPORT.md` — report with scenario results (OK/FAIL/NOTE), conclusions, and recommendations.
- `test_cases/TEST_CASES.md` — executed checks; each failed case references the related bug ID.
- `bugs/BUG_REPORT.md` — scenario-based defect reports with steps, actual result, expected result, severity, and priority.
- `docs/IMPROVEMENTS.md` — improvement suggestions that are not defects.
- `docs/LEGEND.md` — status and severity legend.

## How to read this repository
Test cases and defects are linked by ID: the test-case table shows which execution produced each defect, while the bug report explains what failed and what the expected behavior was. I compared offline and online behavior to separate cache/USB-reading defects from defects in the slides themselves. Bugs are separated by scenario so that a developer can focus only on the relevant videos and artifacts.