# BlacHammer AIO Loader - Official Downloads

Ready-to-run Windows loader and Android companion, created by **BlacHammer**.
This public repository contains download information and legal notices, **not the
application source code**. Development repositories are private.

## Download and install

| Platform | Current version | Direct download |
|---|---|---|
| Windows | 4.0.0, Developer Suite / managed administration | [Download EXE](https://github.com/marese310/BlacHammer-AIO-Loader-Downloads/releases/download/desktop-4.0.0-companion-3.1.0/BlacHammerAIOLoader_v4.0.0.exe) |
| Android 6.0+ | 3.1.0, version code 13 | [Download APK](https://github.com/marese310/BlacHammer-AIO-Loader-Downloads/releases/download/desktop-3.1.0-companion-3.1.0/BlacHammerAIOLoaderCompanion_v3.1.0.apk) |

[All downloads, checksums and release notes](https://github.com/marese310/BlacHammer-AIO-Loader-Downloads/releases/latest)

### Desktop 4.0.0: Developer Suite and managed administration

- Purchasable lifetime Developer Suite unlocks paid/local developer features,
  unlimited licensed PCs and an exportable own-server backend/Discord-bot setup
  kit. Hosting costs are separate; pricing and fulfillment remain manual.
- A purchase never grants official server moderation. Host/Master is reserved
  for the verified Discord server owner's linked Developer license. Alt Staff
  requires a separate GM-approved grant; only the current owner can approve,
  reset or revoke it. Never post license keys, staff keys or bot tokens.
- Original/custom server profiles keep credentials separate. The footer shows
  version, edition and selected server; update checks verify the official signed
  manifest. Custom hosts cannot replace official binary-signing trust.
- Right-side and bottom scrollbars make controls reachable without enlarging
  the window. Use the wheel vertically, Shift+wheel horizontally, or Tab to
  bring focused controls into view.
- Android remains on the existing 3.1.0 release; original maps/assets, private
  imports, paid Asset Hub and phone-to-PC pairing remain supported.

### Maps and original assets restored

- The original 137,818-row Once Human database is bundled on Android and remains
  separately selectable offline. Existing imports, libraries and pairing are preserved.
- Nine map providers/directories, including MapGenie, IGN, th.gl, Gamer Guides,
  OnceHumanDB, iZurvive and HoYoLAB, with Android embedded HTTPS and browser fallback.
  Third-party login, coverage and embedding restrictions still apply.
- **Asset Finder > Shared Asset Hub** on PC/phone: active paid/developer license and
  verified Discord enrollment required. Click Link Discord, then send the one-time
  `!asset link CODE` in your own private Discord customer panel. Never post a key.
- Separate official/customer CSV catalogs; imports create new user libraries.
  Share only authorized CSVs up to 512 KiB, with explicit consent for automatic
  private Discord staff export with creator username/rank and possible publication.
  Existing local/private files are not silently uploaded.
- Online raw GitHub/Discord CSV import, private Discord drafts and scoped,
  paired phone-to-PC MCP asset transfer. No arbitrary paths or code execution.
- Staff moderation/audit, approved-only customer exports and GM-only account
  recovery. Hosted removal cannot erase downloaded copies or unrelated device files.
  New sharing enrollment does not retroactively bind legacy sign-ins.

**“Unknown license key” on a fresh Windows install:** use 3.0.5. Earlier releases
selected the separate custom database rather than the official Keygen account.
The fix uses Keygen on fresh installs and repairs unactivated official empty
profiles; existing custom licenses/servers are preserved. No new key, copied
settings or administrator token is needed. Developer/customer entitlements,
expiry and HWID rules still come from the license issuer.
The official unlimited Dev/Owner policy also receives issuer-side validation
without a fingerprint scope after a mismatch. Only that verified developer
policy can retry this way; customer machine restrictions remain unchanged.

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

For pairing, use the PC's Remote tab with Internet relay, reachable trusted Wi-Fi/LAN,
private VPN or secure Bluetooth. Never expose the
PC Remote API to the public internet. Cloud support works without PC pairing.
Phone imports do not silently overwrite or merge into PC game libraries.

### Internet relay: your phone to your own PC

1. Update both platforms. On your paid PC, enable Remote and **Internet relay**.
   Wait for "Internet relay ready" in Remote activity and open a fresh setup QR.
2. On the phone, scan/paste that card, trust only your own PC and choose
   **Internet relay**. Approve the correct named phone on your PC.
3. Keep the PC/loader awake and both devices online. No developer VPN invitation,
   router forwarding or public PC listening port is needed.

The hosted service forwards encrypted TLS bytes; the phone still verifies your
PC certificate, and PC approvals, tokens and revocation still apply. Keep the QR
private: it contains a separate relay-admission capability, not a license/PC token.
Service is bounded (initially 128 PC rooms, four concurrent streams per PC);
availability depends on hosting resources. Errors are explicit, not an unlimited
connectivity guarantee. Wi-Fi/private VPN/Bluetooth remain separate fallback choices.

### Private VPN for your own devices

Install official [Tailscale](https://tailscale.com/download) on PC and Android and
authorize both in your private tailnet. In PC Remote, refresh LAN / VPN addresses,
select the PC's `100.64.0.0/10` address and scan/paste a fresh setup QR. Choose LAN /
VPN and approve on the PC. Same certificate pinning and revocation; no public ports.
Wi-Fi discovery does not cross the tunnel. Android permits one active VPN; another
VPN can disconnect Tailscale.

PC VPN help supplies a TCP rule scoped to its EXE, port, Tailscale interface and
shared source range (any Windows profile, not unrestricted public-interface access).
Separately restrict tailnet policy to your phone -> PC Remote port; default/other
allow rules may permit more. Keep exit nodes, subnet routing, Serve and Funnel off.
Never invite customers into the owner's personal tailnet. Internet relay is separate;
no bundled/mandatory Tailscale account is required.

### Pair without typing / Bluetooth fallback

1. Update both platforms together. Keep the PC loader open and **Enable Remote**;
   select its actual LAN adapter and open **Scan-to-pair QR**.
2. Phone **Pair PC > Scan PC QR** (or paste the PC's copied setup link), trust only
   your own PC's card, choose Wi-Fi, then approve on the PC. No address/fingerprint/
   code typing. The card contains the PC identity, not a license or login token.
3. A timeout is a network/listener failure before certificate/code validation.
   `192.168.0.x/24` and `192.168.1.x/24` are different subnets unless routed. Use the
   same home router, avoid guest isolation, and check VPN LAN restrictions. PC
   Connection help provides exact EXE/port-scoped Private/LocalSubnet firewall
   commands (TCP selected port, UDP 8766); no automatic public/router openings.
4. Without Wi-Fi: pair PC and phone in Windows/Android **Bluetooth Settings**, enable
   **secure Bluetooth fallback** in PC Remote, reopen its QR, scan and choose
   Bluetooth. Android 12+ asks for Nearby devices permission. A working PC radio/
   driver is required; Bluetooth is opt-in each PC launch.
5. Bluetooth actually carries the same remote dashboard/scripts/logs/assets/chat/
   developer APIs over bonded/encrypted RFCOMM plus certificate-pinned TLS, with PC
   approval and revocation. Cloud/Discord/Steam/translation/updates still require
   Internet. Keep setup cards private and scan again after address/identity changes.

Manual address/fingerprint/code entry remains available. Re-pair older HTTP
connections. If port 8765 is occupied, choose an unused port; never kill another app.

Companion 3.0.5 shows the actual Wi-Fi failure in the fallback dialog; Bluetooth
errors distinguish bonding/permission, connection/deadline, certificate verification
and authenticated API rejection. The Bluetooth offer is not itself a Bluetooth error.

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
been checked. PC-generated QR decoding, real TLS stream pin/approval/revocation tests
and native Windows Bluetooth service registration passed. The signed APK was installed/
upgraded on Android 15 in an emulator, paired via pinned HTTPS to the running PC EXE,
approved on PC and reached its authenticated dashboard. Two on-device tests exercised
Android HTTPS remote routes and the Bluetooth TLS engine over an encrypted stream.
The released EXE/APK passed public HTTPS relay pairing, named PC approval,
authenticated dashboard and pairing persistence after app restart on an emulator
and a real Galaxy Z Fold5. Android-provider public-relay tests also checked token
revocation and wrong-pin rejection. No customer scripts were run.
Physical Bluetooth, cellular-only operation and every customer's network remain
separate tests; initial hosted capacity is bounded, not unlimited.
Translation requires a separately configured provider.
Hosting availability, license entitlement and payment readiness are separate checks.

The Android signer SHA-256 is:
`7e847a39a105fd1ec17e49693b92cfb226a28edccfb79694155e53ac7af8cb80`.

## License

Source-available commercial software, not open source. Free download does not grant
paid/developer access or permission to fork, rebrand or redistribute derivative builds.
See [LICENSE](./LICENSE), [third-party notices](./THIRD_PARTY_NOTICES.txt) and the
third-party license documents distributed alongside the downloads. Third-party rights
remain separate. No customer data, admin credentials or signing keys are distributed.
