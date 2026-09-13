# Cache Testing Results

Device: Android TV, 4K UHD | Recording method: Screen Record  
Execution mode: cache enabled for all scenarios | Date: 29.07.26

## 1. Scenario Results

### Scenario 1 — Slideshow

#### SL-0011808

**[OK]** Slide content is displayed; no visible image underloading was observed. The issues are behavioral.

**[FAIL]**
- Application freezes during playback at 00:35 and 02:20.
- Application lag at 04:14.

**[NOTE]**
- Lag during slide transitions is a smoothness defect rather than a content-loading defect.
- Without device logs, the cause of the freezes cannot be isolated; a run with logs or on an emulator is required.

#### SL-0011810

**[OK]** Some content is displayed and slide transitions occur.

**[FAIL]**
- The image in the center of the slide does not load, leaving a white area at 03:48.
- The slide loads in parts and a white area remains in the center at 05:30.

**[NOTE]**
- Image-loading lag at 00:14–00:18; loading artifact at 01:18–01:21.
- Fragments of the previous slide remain over the new slide during transitions at 02:18, 02:27–02:30, and 02:45.
- The right side of the slide loads before the left side at 06:10.
- The price tag extends beyond the circular frame at 06:47; see IMP-001.

#### SL-0011650

**[OK]** Slides containing video open.

**[FAIL]**
- Video does not load at 00:50.

**[NOTE]**
- Video playback lags at 00:25–00:40 and loads slowly with lag at 01:19–01:40.

#### SL-0011800

**[OK]** Playback starts before the crash occurs.

**[FAIL]**
- Application crash at 00:24.
- Application crash at 00:54.

**[NOTE]**
- The crashes reproduced twice in one run; crash-report analysis is required.

#### SL-0011643

**[OK]** The “no such slideshow” message is displayed, which is the expected response for a nonexistent ID.

**[FAIL]** —

**[NOTE]** Not a bug: nonexistent-slideshow validation worked correctly.

#### SL-0011644

**[OK]** The “no such slideshow” message is displayed, which is the expected response for a nonexistent ID.

**[FAIL]** —

**[NOTE]** Not a bug: nonexistent-slideshow validation worked correctly.

#### SL-74367 (su)

**[OK]** Slides are displayed.

**[FAIL]** —

**[NOTE]** Lag occurs during slide-to-slide transitions at 02:10–02:19.

### Scenario 2 — Slideshow

#### SL-0011809

**[OK]** Slides eventually render.

**[FAIL]** —

**[NOTE]**
- Long loading time with elements appearing progressively at 00:20.
- Freezes while loading the map at 01:55 and weather widget at 02:18.

#### SL-0011650

**[OK]** Slides open and some widgets render.

**[FAIL]**
- The upper-left widget does not load at 00:55.
- Slide playback freezes at 02:16.

**[NOTE]** The bottom-left video loads slowly and lags at 01:26.

#### SL-0011645

**[OK]** Some slide objects are displayed.

**[FAIL]**
- An image on the left does not load, leaving a white area at 02:34.
- White areas remain in the center at 04:00 and 06:06.

**[NOTE]**
- Objects finish loading with a small freeze at 01:59–02:06.
- The right side of the slide loads before the left side at 06:26.

#### SL-0011646

**[OK]** Slides are displayed.

**[FAIL]** —

**[NOTE]**
- Dessert-image animation freezes at 02:25.
- Slide transitions freeze at 03:26.

#### SL-07473 (su)

**[OK]** Slides are displayed.

**[FAIL]** —

**[NOTE]** Slide transitions freeze at 00:25 and 00:32.

### Scenario 3 — Full Offline Mode (USB)

#### SL-0011946 — offline from the cache folder

**[OK]** The slideshow opens when it is placed in the application cache folder on the USB drive.

**[FAIL]**
- Some images are not displayed and videos do not load.

**[NOTE]**
- Cross-check: the same slideshow works correctly online when launched by ID, so the defect is specific to offline reading.
- The slideshow is not found when stored outside the application cache folder.

#### SL-0011961 — offline from the cache folder

**[OK]** The slideshow opens when it is placed in the application cache folder.

**[FAIL]**
- Slide navigation hangs and videos do not play.

**[NOTE]** Offline playback is effectively unusable despite correct file placement.

#### File placement condition — general

**[OK]** Offline launch is possible.

**[FAIL]** —

**[NOTE]**
- It works ONLY when files are stored in the application's dedicated cache folder on the USB drive, not in any other folder.
- The requirement is not intuitive and the UI gives no path hint, so the user has to discover it by trial and error.

### Scenario 4 — Collections

#### Collection 72323

**[OK]** The collection opens and some slides are displayed.

**[FAIL]**
- Part of a slide does not load and remains white at 01:32.

**[NOTE]**
- Loading is visibly progressive with lag from top to bottom at 00:16–00:22; transition lag occurs at 00:47 and 01:32.
- It is unclear whether the white area should contain content, so comparison with the source slide is required.

#### Collection 0011656

**[OK]** The collection is displayed.

**[FAIL]** —

**[NOTE]**
- Minor lag in the bottom-left video at 01:18.
- Small transition freezes at 01:59.

#### Collection 0011651

**[OK]** —

**[FAIL]**
- Collection not found.

**[NOTE]** Test data/environment issue, not a code defect; requires confirmation from the customer.

### Scenario 5 — Streams

#### Stream 75376 (su)

**[OK]** Stream status is displayed.

**[FAIL]**
- When the status is “Access denied”, there is no password input or action, so the stream cannot be unlocked.

**[NOTE]** Even when the password is known, the stream cannot be unlocked because the input UI is missing.

#### SL-0011811 — stream 0011660

**[OK]** Everything is displayed correctly and no defects were observed.

**[FAIL]** —

**[NOTE]** No issues: playback and loading behave correctly.

#### Stream 0011653 → SL-0011649

**[OK]** —

**[FAIL]**
- The stream does not exist in the environment.

**[NOTE]** Test data/environment issue, not a code defect; requires confirmation from the customer.

## 2. Overall Conclusions

- Scenario 1: application freezes and lag in 0011808; white areas and residual artifacts in 0011810; video loading/playback issues in 0011650; two reproducible crashes in 0011800, rated Critical; 0011643/0011644 correctly validate nonexistent IDs.
- Scenario 2: progressive loading and widget freezes in 0011809; missing widget plus slide freeze in 0011650; repeated white areas in 0011645; animation and transition freezes in 0011646 and 07473.
- Scenario 3: offline mode launches ONLY from the application cache folder on USB, which is non-intuitive and undocumented in the UI; even with correct placement, playback is unreliable — 0011961 hangs with no video, and 0011946 misses media while online mode works.
- Scenario 4: loading/transition lag plus a white area in 72323; minor video lag and transition freezes in 0011656; collection 0011651 is missing from the environment.
- Scenario 5: 0011811 works without observed defects; 75376 has no password-entry UI; stream 0011653 does not exist in the environment.
- Cross-cutting patterns: white areas caused by incomplete image loading; transition lag/freezes; partial/progressive loading; video issues; offline playback remains unstable even when files are placed correctly.
- Release risks: application crashes rated Critical; offline mode combines an undocumented placement requirement with playback defects; protected streams cannot be unlocked through the UI.

## 3. Recommendations

**Image and media loading**
- Fix repeated incomplete loading that leaves white areas in 0011810, 0011645, and collection 72323. Either preload content within the slide timing or provide graceful degradation without a persistent white placeholder.
- Ensure reliable video loading/playback in 0011650 and 0011656 and load widgets without freezes in 0011809 and 0011650.

**Offline mode — High**
- Accept slideshow files from any USB folder or explicitly show the required path in the UI. The current behavior depends on a dedicated cache folder discovered by trial and error.
- Fix offline playback in 0011961, where slide navigation hangs and video is unavailable, and in 0011946, where media is missing even though the same slideshow works online.

**Stability — Critical/High**
- Investigate crashes in 0011800 using crash reports and analyze application/slide freezes in 0011808 and 0011650.

**Transition performance**
- Profile slide transitions because lag/freezes appear across multiple scenarios; remove residual previous-slide artifacts in 0011810.

**Streams — High**
- Add password entry/unlock UI for the “Access denied” state in stream 75376.

**UI / layout**
- Align the price tag within the circular frame in 0011810, tracked as IMP-001, and fix animation freezes in 0011646.

**Test data / environment — customer confirmation required**
- Confirm whether stream 0011653 and collection 0011651 should exist in the environment, then execute those scenarios separately.