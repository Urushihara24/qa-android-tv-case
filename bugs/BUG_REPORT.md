# Bug Reports by Scenario

### BUG-001 — Application freezes

- Scenario 1 · 0011808 · Major / High · Open
- Steps: launch 0011808 with cache enabled and play the slideshow.
- Actual: freezes at 00:35 and 02:20; application lag at 04:14.
- Expected: playback without freezes or lag.

### BUG-002 — Lag/freezes during slide transitions

- Scenario 1 · 0011808, 74367 (su) · Major / High · Open
- Steps: switch between slides in 0011808 and 74367.
- Actual: transition lag in 0011808; lag in 74367 at 02:10–02:19.
- Expected: smooth transitions without lag.

### BUG-003 — White area instead of an image

- Scenario 1 · 0011810 · Major / High · Open
- Steps: play 0011810 and observe image loading.
- Actual: white area in the center at 03:48; content loads partially and a white area remains at 05:30.
- Expected: images load completely within the slide timing.

### BUG-004 — Previous-slide artifacts remain during transitions

- Scenario 1 · 0011810 · Major / High · Open
- Steps: switch between slides in 0011810.
- Actual: fragments of the previous slide remain over the new slide at 02:18, 02:27–02:30, and 02:45.
- Expected: the previous slide is fully replaced without residual artifacts.

### BUG-005 — Partial/progressive slide loading

- Scenario 1 · 0011810 · Major / Medium · Open
- Steps: observe slide loading in 0011810.
- Actual: the right side loads first and the left side follows later at 06:10.
- Expected: the full slide appears together without visibly delayed content.

### BUG-006 — Freezes/artifacts while loading a slide

- Scenario 1 · 0011810 · Minor / Medium · Open
- Steps: observe slide loading in 0011810.
- Actual: image-loading lag at 00:14–00:18; loading artifact at 01:18–01:21.
- Expected: loading without freezes or artifacts.

### BUG-007 — Video does not load or lags

- Scenario 1 · 0011650 · Major / Medium · Open
- Steps: play video slides in 0011650.
- Actual: video lags at 00:25–00:40, fails to load at 00:50, and loads slowly with lag at 01:19–01:40.
- Expected: video loads and plays smoothly.

### BUG-008 — Application crashes

- Scenario 1 · 0011800 · Critical / High · Open
- Steps: launch 0011800 with cache enabled and play it.
- Actual: two application crashes at 00:24 and 00:54.
- Expected: playback completes without application termination.

### BUG-009 — Partial/progressive slide loading

- Scenario 2 · 0011809, 0011645 · Major / Medium · Open
- Steps: observe loading in 0011809 and 0011645.
- Actual: progressive loading in 0011809 at 00:20; right side loads before the left side in 0011645 at 06:26.
- Expected: the entire slide appears together.

### BUG-010 — Widget loading freezes / widget does not load

- Scenario 2 · 0011809, 0011650 · Minor / Medium · Open
- Steps: observe widget loading in 0011809 and 0011650.
- Actual: map freezes in 0011809 at 01:55, weather widget freezes at 02:18, and the upper-left widget in 0011650 does not load at 00:55.
- Expected: widgets load fully without freezes.

### BUG-011 — Video does not load or lags

- Scenario 2 · 0011650 · Major / Medium · Open
- Steps: play video slides in 0011650.
- Actual: the bottom-left video takes a long time to load and lags at 01:26.
- Expected: video loads and plays smoothly.

### BUG-012 — Slide/playback freezes

- Scenario 2 · 0011650 · Major / High · Open
- Steps: play 0011650.
- Actual: slide playback freezes at 02:16.
- Expected: playback continues without freezing.

### BUG-013 — White area instead of an image

- Scenario 2 · 0011645 · Major / High · Open
- Steps: play 0011645 and observe loading.
- Actual: white area on the left at 02:34 and in the center at 04:00 and 06:06.
- Expected: images load completely.

### BUG-014 — Freezes/artifacts while loading a slide

- Scenario 2 · 0011645 · Minor / Medium · Open
- Steps: observe loading in 0011645.
- Actual: objects finish loading with a freeze at 01:59–02:06.
- Expected: loading without freezes.

### BUG-015 — Image animation freezes

- Scenario 2 · 0011646 · Minor / Low · Open
- Steps: observe animation in 0011646.
- Actual: animation freezes at 02:25.
- Expected: smooth animation without freezing.

### BUG-016 — Lag/freezes during slide transitions

- Scenario 2 · 0011646, 07473 (su) · Major / High · Open
- Steps: switch slides in 0011646 and 07473.
- Actual: transition freezes in 0011646 at 03:26 and in 07473 at 00:25 and 00:32.
- Expected: smooth transitions without freezes.

### BUG-017 — Offline slideshows work only from the application cache folder on USB, with no path hint

- Scenario 3 · 0011946, 0011961 · Major / High · Open
- Steps: place files outside the application cache folder on the USB drive and press USB; then place the same files inside the cache folder and retry.
- Actual: outside the cache folder the application reports that no slideshows were found; inside the cache folder the slideshow launches. The UI does not explain the required path.
- Expected: the application finds slideshows regardless of folder, or clearly states the required USB path in the UI.

### BUG-018 — White area instead of an image

- Scenario 4 · collection 72323 · Major / High · Open
- Steps: play collection 72323 and observe loading.
- Actual: part of a slide fails to load and remains white at 01:32.
- Expected: all slide elements load completely.

### BUG-019 — Partial/progressive slide loading

- Scenario 4 · collection 72323 · Major / Medium · Open
- Steps: observe collection 72323 while it loads.
- Actual: the page loads from top to bottom with lag at 00:16–00:22.
- Expected: the page appears as a complete composition without delayed sections.

### BUG-020 — Video does not load or lags

- Scenario 4 · collection 0011656 · Major / Medium · Open
- Steps: play collection 0011656.
- Actual: minor lag in the bottom-left video at 01:18.
- Expected: smooth video playback.

### BUG-021 — Lag/freezes during slide transitions

- Scenario 4 · collection 72323, collection 0011656 · Major / High · Open
- Steps: switch slides in collections 72323 and 0011656.
- Actual: transition lag in 72323 at 00:47 and 01:32; freezes in 0011656 at 01:59.
- Expected: smooth transitions without lag or freezes.

### BUG-022 — “Access denied” with no way to enter a password

- Scenario 5 · stream 75376 (su) · Major / High · Open
- Steps: open protected stream 75376.
- Actual: the status shows “Access denied”, but no password field or action is available, so the stream cannot be unlocked.
- Expected: an “Access denied” state provides a password entry form.

### BUG-023 — Offline slide navigation hangs and videos do not play

- Scenario 3 · 0011961 · Major / High · Open
- Steps: place 0011961 in the application cache folder on a USB drive; launch through the USB option without internet access; navigate through slides.
- Actual: slide navigation hangs and videos do not play.
- Expected: offline slides advance without freezes and videos play correctly.

### BUG-024 — Offline images and videos fail to load while the same slideshow works online

- Scenario 3 · 0011946 · Major / High · Open
- Steps: place 0011946 in the application cache folder; launch through USB without internet access; compare with launching the same slideshow by ID online.
- Actual: offline mode misses some images and videos, while the same slideshow works correctly online.
- Expected: offline images and videos load with the same content completeness as online playback.