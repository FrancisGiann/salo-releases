# Salo Android test downloads

Salo is a private food-choice app for Android. This public repository is for binary test downloads and release information only; it does not publish the application source code.

## Current prerelease

The prerelease is **Salo 0.2.0 Android test**, tag `v0.2.0-test` (app version `0.2.0+2`). Download the `salo-0.2.0-release-arm64.apk` asset from this repository’s Releases page and verify it against the attached `SHA256SUMS.txt` before installation.

The APK is a release-mode Flutter AOT test build signed with the existing Android debug certificate. The certificate is not a production signing identity. It supports Android 8.0 (API 26) or newer on **arm64-v8a** devices. It is not a Google Play package, is not automatically updated, and will not notify you of future versions. Install manually only if you are comfortable testing an APK outside Google Play. AOT compilation omits readable debug kernel and source snapshots, but compiled binaries can still be reverse engineered. This prerelease does not grant an open-source licence to the Salo application; the ODbL terms for the embedded data are described in [`NOTICE.md`](NOTICE.md).

## Data and coverage

The APK bundles 293 named OpenStreetMap-derived food-category map records from a bounded selection area: latitude 13.82–14.17, longitude 121.43–121.78. The data snapshot cutoff is 2026-10-30 21:24:51 UTC; the extract was retrieved 2026-10-31. The catalogue is incomplete, may include duplicate representations, and does not verify that a place is open or operating. From the app’s approximate city centres, 83 Lucena and 35 Tayabas map records fall within 3 km. These counts are not counts of unique businesses. Four café name benchmarks were not matched in this bounded extract; that does not show they are absent from all OpenStreetMap data or do not exist. Photos, opening hours and prices may be unknown. See [`NOTICE.md`](NOTICE.md) for attribution and data terms.

## Feature and test limits

Nearby discovery reads the bundled catalogue; Google Places is not configured or called. Google billing and credentials are not included. Directions open an external maps app only when tapped. Two-person practice works on one phone; remote two-device rooms are not configured. User-added places stay in the app’s local private storage.

The application verification run passed 34 Flutter tests and 9 offline catalogue-extractor tests. The local pairing fixture’s 13 tests were not rerun for this release. This is not a physical-device, TalkBack, performance or remote-pairing certification.
