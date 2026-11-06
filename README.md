# BlacHammer AIO Loader - Official Downloads

Ready-to-run Windows loader and Android companion, created by **BlacHammer**.
This public repository contains download information and legal notices, **not the
application source code**. Development repositories are private.

## Download and install

| Platform | Current version | Direct download |
|---|---|---|
| Windows | 3.0.1, secure pairing/live notices/signed updates | [Download EXE](https://github.com/marese310/BlacHammer-AIO-Loader-Downloads/releases/download/desktop-3.0.1-companion-3.0.3/BlacHammerAIOLoader_v3.0.1.exe) |
| Android 6.0+ | 3.0.3, version code 8 | [Download APK](https://github.com/marese310/BlacHammer-AIO-Loader-Downloads/releases/download/desktop-3.0.1-companion-3.0.3/BlacHammerAIOLoaderCompanion_v3.0.3.apk) |

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
  documentation/legal notices and the empty public script catalog, not the loader
  or companion implementation.

## Features and access

- Premium navy/cyan/gold Android interface with readable controls, dashboard tiles,
  quick navigation, ripple/entry animations and a branded splash. Android animation
  settings are respected; no decorative loading delay when animations are disabled.
- Refreshed Windows EXE fixes the retired Community URL and isolates frozen restarts
  so the old instance does not clean up the new instance's temporary files.
- The public script catalog is intentionally empty while application source/examples
  remain private. Licensed chat and customer-assigned downloads are separate.
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

Update both platforms together. Enable PC Remote, copy its HTTPS address and certificate
fingerprint into phone Pairing, compare the fingerprint on the PC, then request approval.
Re-pair older HTTP connections. Allow the EXE only on Windows Firewall Private/LocalSubnet
(selected TCP port, discovery UDP 8766). If 8765 is occupied, choose an unused port.

Open Support, enter a message, consent and submit New ticket; merely opening Support
does not send anything. Notices/reply alerts poll while the apps are open, not as guaranteed
background OS push. Android/Windows private inboxes remain separate.

Automatic updates default on and can be disabled. Only newer official releases with a
valid owner-signed manifest and matching checksum/size are accepted. Windows waits for
five idle minutes, a further 60-second postponement window and no running tools/scripts,
or normal exit; the replaced EXE is backed up. No background scheduler/elevated service is
installed, so a closed app checks next time it opens. Android downloads verified APKs,
but installation still requires Android permission and approval. Older builds need this
initial upgrade manually. The detached update signatures do not replace Windows
Authenticode signing; SmartScreen warnings may still appear.

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
