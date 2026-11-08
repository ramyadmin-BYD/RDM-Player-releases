# RDM Player — Releases

Signed Android APKs of **RDM Player**, a music and radio player designed for in-car Android head units.

This repository only distributes release files. The source code is kept in a separate private repository and is **not** published here. The "Source code" zip files GitHub attaches to each release contain only this README.

## Install or update

- **Latest version:** [Releases → Latest](../../releases/latest). Download `RDM-Player-vX.Y.Z-release.apk`.
- **Already on 1.1.0 or newer:** the app finds new versions by itself (Settings → Software updates). No GitHub account is needed.
- **On 1.0.0:** that version has no built-in updater. Install the latest APK once by hand. It installs over 1.0.0 without uninstalling, and your settings and library are kept.

Android always asks you to confirm an installation. The app never installs anything silently.

## Verify a download

Every release includes `SHA256.txt`.

```bash
shasum -a 256 RDM-Player-vX.Y.Z-release.apk
```

Every RDM Player release is signed with the same certificate:

```
SHA-256: c4ce21d7360be430dc2d455051e1d73c8933cef7137b4ef2a8e23e5dd3507850
```

The in-app updater checks all of the following. It refuses any download that fails a check:

- the checksum;
- the package name (`com.rdm.player`);
- the signing certificate, which must be the one above;
- the version, which must be newer than the installed one.

## Notes

- Compatibility with BYD DiLink head units has not been verified on vehicle hardware.
- RDM Player is an independent project. It is not affiliated with, or endorsed by, BYD.
- The app contains no tracking or telemetry.
