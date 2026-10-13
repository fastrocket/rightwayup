# iOS readiness: RightWayUp

Checked October 13, 2026.

## Current state

This repo contains model/library code, browser support and Core ML model artifacts, but no iOS app project or App Store client.

## Work to complete

1. Define the first iOS workflow: choose/capture image, estimate rotation, display confidence/abstention, preview correction, and save/share a corrected copy.
2. Choose which Core ML tier(s) ship in the app and whether any model is downloaded. Document model sizes, supported devices and offline behavior. Prefer on-device image processing and disclose any upload explicitly.
3. Implement a native Swift/SwiftUI client that applies the matching calibrated thresholds, preserves EXIF/orientation/color metadata, never overwrites the source image, handles large files under memory pressure, and exposes abstention clearly.
4. Add a licensed fixture-based validation set for orientation and abstention behavior. Check HEIC/JPEG/large images, offline use, photo permissions, save/share, VoiceOver and background/resume on physical iPhones/iPads.
5. Establish bundle ID/ASC app record, deployment target, privacy manifest, permissions, age rating, screenshots, support/privacy URLs and review notes before TestFlight.

## Repo guidance

The model card and `FREEZE.md` are authoritative for model/calibration behavior. Credits in the project name ORTUS AI; this checkout is `fastrocket/rightwayup`.

## Completion record

Update this file with the source commit, bundle ID, marketing version/build, Xcode and SDK versions, archive-policy result, upload time, App Store Connect processing state, TestFlight group/tester availability, and physical-device results. Treat upload, processing, TestFlight availability, App Review submission, approval, and public release as separate states. Do not include secrets or signing materials.
