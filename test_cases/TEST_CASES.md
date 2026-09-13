# Test Cases

| TC | Scenario | Object | Input field | Mode | Actual result | Status | Bug ID |
|----|----------|--------|-------------|------|---------------|--------|--------|
| TC-01 | 1 | 0011808 | Slideshow | cached | Freezes (00:35, 02:20), transition lag, application lag (04:14) | Fail | BUG-001, BUG-002 |
| TC-02 | 1 | 0011810 | Slideshow | cached | White areas (03:48, 05:30), residual artifacts, partial loading, price tag outside the frame | Fail | BUG-003, BUG-004, BUG-005, BUG-006 |
| TC-03 | 1 | 0011650 | Slideshow | cached | Video does not load / lags (00:25–01:40) | Fail | BUG-007 |
| TC-04 | 1 | 0011800 | Slideshow | cached | Two application crashes (00:24, 00:54) | Fail | BUG-008 |
| TC-05 | 1 | 0011643 | Slideshow | cached | “No such slideshow” — expected response for a nonexistent ID | Pass | |
| TC-06 | 1 | 0011644 | Slideshow | cached | “No such slideshow” — expected response for a nonexistent ID | Pass | |
| TC-07 | 1 | 74367 (su) | Slideshow | cached | Transition lag (02:10–02:19) | Fail | BUG-002 |
| TC-08 | 2 | 0011809 | Slideshow | cached | Progressive loading (00:20), map/weather widget freezes | Fail | BUG-009, BUG-010 |
| TC-09 | 2 | 0011650 | Slideshow | cached | Widget does not load (00:55), video lags (01:26), slide freezes (02:16) | Fail | BUG-010, BUG-011, BUG-012 |
| TC-10 | 2 | 0011645 | Slideshow | cached | White areas (02:34, 04:00, 06:06), partial loading | Fail | BUG-009, BUG-013, BUG-014 |
| TC-11 | 2 | 0011646 | Slideshow | cached | Animation freeze (02:25), transition freezes (03:26) | Fail | BUG-015, BUG-016 |
| TC-12 | 2 | 07473 (su) | Slideshow | cached | Transition freezes (00:25, 00:32) | Fail | BUG-016 |
| TC-13 | 3 | 0011946 | USB connection | offline | Some images are missing and videos do not load (online works); slideshow is not found outside the cache folder | Fail | BUG-017, BUG-024 |
| TC-14 | 3 | 0011961 | USB connection | offline | Slide navigation hangs, videos do not play; slideshow is not found outside the cache folder | Fail | BUG-017, BUG-023 |
| TC-15 | 4 | collection 72323 | Slideshow menu | cached | Top-to-bottom loading lag, white area (01:32) | Fail | BUG-018, BUG-019, BUG-021 |
| TC-16 | 4 | collection 0011656 | Slideshow menu | cached | Minor video lag (01:18), transition freezes (01:59) | Fail | BUG-020, BUG-021 |
| TC-17 | 4 | collection 0011651 | Slideshow menu | cached | Collection not found (test data/environment) | Blocked | |
| TC-18 | 5 | stream 75376 (su) | Scheduled launch | cached | “Access denied” with no way to enter a password | Fail | BUG-022 |
| TC-19 | 5 | slideshow 0011811 (stream 0011660) | Scheduled launch | cached | Works correctly; no defects observed | Pass | |
| TC-20 | 5 | stream 0011653 | Scheduled launch | cached | Stream does not exist in the environment (test data/environment) | Blocked | |