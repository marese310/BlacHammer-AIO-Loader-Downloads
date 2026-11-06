# BlacHammer AIO Loader - Official Downloads

Ready-to-run Windows loader and Android companion, created by **BlacHammer**.
This public repository contains download information and legal notices, **not the
application source code**. Development repositories are private.

## Download and install

| Platform | Current version | Direct download |
|---|---|---|
| Windows | 3.0.0, refreshed companion integration build | [Download EXE](https://github.com/marese310/BlacHammer-AIO-Loader-Downloads/releases/download/desktop-3.0.0-companion-3.0.1/BlacHammerAIOLoader_v3.0.0.exe) |
| Android 6.0+ | 3.0.1, version code 6 | [Download APK](https://github.com/marese310/BlacHammer-AIO-Loader-Downloads/releases/download/desktop-3.0.0-companion-3.0.1/BlacHammerAIOLoaderCompanion_v3.0.1.apk) |

[All downloads, checksums and release notes](https://github.com/marese310/BlacHammer-AIO-Loader-Downloads/releases/latest)

- **Windows:** put the EXE in its own folder and launch it. No build scripts or Python
  installation are needed to open the loader. Running your own Python scripts still
  requires a Python interpreter. Windows may warn because the EXE is not
  Authenticode-signed; verify its SHA-256 against the release checksums.
- **Android:** download the APK and allow installation from your browser if prompted.
  Install over the existing companion; do not uninstall or clear data if you want to
  retain pairing, imported game libraries and the private support inbox. The application
  ID and original release signing certificate are retained.
- No building, Git, Gradle or development tools are needed to install these downloads.
- GitHub's automatic "Source code" archives contain only this download repository's
  documentation/legal notices, not the loader or companion implementation.

## Features and access

- Separate per-game asset libraries, optional Steam metadata/covers and map viewing.
- Separate cloud-service and paired-PC connection indicators.
- Android read-only paired-PC asset browsing and licensed shared Community chat.
- Private Discord-backed support, staff replies and announcements.
- English-default core navigation languages and optional, consent-based translation
  using your own LibreTranslate-compatible provider. No shared provider is bundled.
- Free asset/map features; paid Windows features require a valid purchased key.
  Checkout is disabled until configured. Staff verify payment and issue keys manually.
- Windows-only execution, development, memory and administration tools remain on PC.
  This companion is not a native Android implementation of every Windows tool.

For pairing, use the PC's Remote tab on the same trusted Wi-Fi/LAN. Never expose the
PC Remote API to the public internet. Cloud support works without PC pairing.
Phone imports do not silently overwrite or merge into PC game libraries.

## Support and purchase

[Join the BlacHammer Discord](https://discord.gg/qeGAX6VCUz).
Do not post license keys, pairing tokens, private support identities or credentials in
public issues. Use the app's private support screen for customer-specific problems.

## Verification and release status

Builds, unit tests, release lint, APK certificate and published download hashes have
been checked. Physical Android install/upgrade/UI testing remains unverified because
no phone or emulator was connected. Translation requires a separately configured provider.
Hosting availability, license entitlement and payment readiness are separate checks.

The Android signer SHA-256 is:
`7e847a39a105fd1ec17e49693b92cfb226a28edccfb79694155e53ac7af8cb80`.

## License

Source-available commercial software, not open source. Free download does not grant
paid/developer access or permission to fork, rebrand or redistribute derivative builds.
See [LICENSE](./LICENSE), [third-party notices](./THIRD_PARTY_NOTICES.txt) and the
third-party license documents distributed alongside the downloads. Third-party rights
remain separate. No customer data, admin credentials or signing keys are distributed.
