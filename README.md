# Steward Capture development releases

Direct development builds of the Steward Capture menu-bar app for macOS. The source repository is private. This repository contains download artifacts and release metadata only; there is no App Store distribution.

## Install

Download the ZIP from [the latest release](https://github.com/alexandrethsilva/steward-capture-releases/releases/latest), extract it, and place `Steward Capture.app` in `~/Applications`. Current builds target Apple silicon and macOS 13 or later.

These are development builds with ad-hoc Apple code signatures, not Apple-notarized distribution builds.

## Updates

After the initial installation, the app checks this repository's signed feed hourly, downloads newer builds, finishes its active capture request, and installs and restarts automatically. Only one live app instance can own the local capture store. Update checks do not send captured usage.

The app verifies both the feed and update archive against its pinned Ed25519 key. Failed verification leaves the existing installation in place. The public update verification key is:

```
ymrTF2ZDSRERaS+ZY7QK0QBg93RfcnPJEN+PTp3pqW4=
```

Each release includes `release.json` with its build number, source revision and SHA-256 artifact hashes. Published versions are immutable. The local capture store and capture consent remain outside the application bundle.
