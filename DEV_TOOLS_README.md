# BlacHammer AIO Loader - Developer and Host Manual

Community: **Modz me up**. This loader is for multiple games, software and tools,
not a single game. This guide describes the desktop controls, linked Discord
sign-in, license issuance and isolated hosting. Keep all real credentials private.

**Current stable:** desktop 4.2.0 / Companion 3.2.0.
New users should begin with the [User Guide](USER_GUIDE.md).
Approved private source contributors should follow the separate Contributor
Setup and Build Guide supplied with their private source handoff; an owner-issued
license is still required for paid/Developer activation. Receiving source never
grants official-server administration or production credentials.

**Sharing boundary:** local scripts/tools are not silently copied to GMs.
Current private moderation/export applies to explicitly shared CSV asset data.
Explicit script submission, private GM code review and approval before public
publication are queued for the next update, **not available in 4.2.0**.
Neither current CSV approval nor future code review guarantees code safety.

## Portable tools and phone workspace (4.2.0 / Android 3.2.0)

**Tools** registers native executables and command scripts. **Plugins** registers
DLLs/configs/resources with an optional compatible launcher. **Set launcher**
selects that program; arguments belong to the registration. Dropping a DLL never
injects it. Existing Developer-only DLL Injector permissions are unchanged.
**Relink file** repairs an ambiguous/missing registration explicitly. A remembered
file can rename itself in the same folder and extension; file-ID matching allows
self-modification, with exact size/hash fallback. Multiple matches fail closed.
Legacy entries without an identity must be relinked once if their path is gone.

Each registered tool/plugin can run alongside other utilities and scripts.
**Output** displays its captured stdout/stderr; **Debug** highlights reported
errors/nonzero exits. This monitors loader-launched processes, not every Windows
application, hidden GUI errors or crash dumps. A configured launcher must accept
the resource path; the loader cannot invent a DLL/config protocol. Native GUI
programs retain their own windows; Scripts can **Release GUI to its own window**
without stopping the registered process.

Double-click a file row to run. Drops require confirmation and register originals
in place: Python/protected scripts and folders to Scripts, executable/command
files to Tools, CSV to a new asset library, everything else to Plugins/resources.
No drop executes code, moves the original or bypasses delivery/edition checks.

On a paired Android phone, Dashboard shows running programs; script logs send
bounded stdin text only to registered running scripts that read standard input.
For GUIs open **Portable workspace** after explicitly approving primary-screen
viewing on the PC **Remote** page. Input requires separate PC permission and the
phone checkbox. Approval is for **all paired phones**, session-only, ten minutes;
close sensitive windows first. Stop from either device. Remote off, device
revocation, code rotation, UI rebuild or restart clears approval. Phone pause
clears the preview and phone input checkbox, but does not stop PC scripts.

Screen preview is at most 960x540 JPEG, one frame per second, with fresh-frame
input validation and bounded keys/text/taps/scroll. Existing pinned encrypted
transports and authorization remain required. No gameplay/video-quality stream,
audio, gamepad forwarding, UAC bypass or guaranteed protected-content capture.

## 1. Access levels: know which permission you need

| Access | What it provides | What it does not provide |
|---|---|---|
| Free | Asset Finder and maps | Paid execution, Developer tools or administration |
| Standard paid license | Paid scripts/editor/tools, Community, delivery and companion features | Developer tools or server moderation |
| Developer Suite (`dev`) | Lifetime paid/local Developer features, unlimited licensed PCs, own-server kit export | Official server administration, issuer API credentials or hosting |
| Local owner entitlement (`owner`) | Local Developer capabilities | Automatic Host status or a shared backdoor |
| Host/Master | Developer license linked to the **current Discord server owner**, with approved server grant and online verification | Automatic access to a different host or Keygen issuer token |
| Alt Staff | Developer license plus GM-approved, device/Discord-linked server credential | Permission to issue/reset/revoke staff grants or become Host |
| Bootstrap admin | Initial administration of a new custom server, before first Host enrollment | Access after managed Host adoption or authority on the original host |

Purchasing Developer Suite never grants a Discord moderation role. Key names,
policy labels and Discord role names do not override the license issuer. Only
the current guild owner can approve/reset/revoke Host and Alt Staff grants.
Windows Administrator elevation is separate from all these permissions.

## 2. First sign-in and selecting the right server

1. Download the current official desktop EXE. Keep an existing Android installation
   and its private data; desktop-only changes do not require reinstalling Android.
2. Select **Choose original / custom sign-in server** when necessary.
   The original host uses its official Keygen account. A custom host requires
   that host's HTTPS origin and its own license; official keys are not forwarded.
3. Enter your license key and optional recovery email, then **Sign in**.
   Store the original key securely even if you intend to use Discord afterward.
4. **Remember my key on this device** controls saving the session's key in the
   normal loader configuration. **Log out** removes saved sign-in credentials.
   Discord-login enrollment is a separate server-side setting; logout does not
   disable it.
5. A verified Developer license exposes **Dev Tools** and **DLL Injector**.
   Hosted moderation tabs remain locked until **Server access** verification.

The footer shows the desktop version, edition, verified server role and selected
server. **Check version** verifies the official signed release feed. It reports
up-to-date, update available, preview/ahead, or a visible verification failure.
Use right-side/bottom scrollbars in a small window. Wheel scrolls vertically,
Shift+wheel horizontally, and Tab reveals focused controls.

## 3. Link a license to its real Discord owner

This links the license to a Discord account, not just an editable username.

1. Sign in with the license on the intended PC.
2. Open **Asset Finder > Shared Asset Hub > Link Discord**.
   Developers can also use **Dev Tools > Server access > 1. Link Discord**.
3. In **Modz me up**, use `!apply customer` in **help-desk** if you do not have
   your own private customer panel. Follow the bot's private-panel link.
4. Copy the displayed temporary command into **your own private panel**:

   ```text
   !asset link LINK_CODE
   ```

5. Wait for the bot to confirm ownership. Return to the loader and Refresh.

The link code expires in ten minutes. Do not send the license key, device token,
staff credential or bot token to Discord. Linking another installation must
use the already associated account. Changing the association requires GM recovery.
Linking does not remove customer HWID locks or create server privileges.

## 4. Enable and use Discord sign-in

Discord sign-in is a **private bot-approved login**, not a username/password
field, Discord password collection, or a promise of browser OAuth.

### One-time enrollment

1. First sign in with your license key and complete section 3.
2. In **Shared Asset Hub**, click **Enable Discord sign-in** and confirm.
3. The selected host stores an encrypted license credential so it can recheck
   the original issuer during future sign-ins. Enrollment is explicit and
   per-license/per-host; only enable it on a host you trust.

### Future sign-in without typing the key

1. On the loader sign-in screen choose **Sign in with Discord (linked licenses)**.
2. Click **Copy approval command**. In your own private panel send:

   ```text
   !login SIGNIN_CODE
   ```

3. Only approve a code generated on **your own PC**. The loader/bot show a
   device identifier; never approve a code somebody sends you.
4. After the bot confirms, return to that loader and click **Check approval**.
5. The host rechecks the linked account, active license and PC HWID. The client
   then performs its normal online license activation before opening paid tools.

Codes expire in five minutes and are single-use. The private polling capability
never needs to be pasted anywhere. If several licenses are enabled for one
Discord account, the bot lists only their hashed member IDs. Choose explicitly:

```text
!login SIGNIN_CODE HASHED_MEMBER_ID
```

### Disable and recover

- **Shared Asset Hub > Disable Discord sign-in** removes that server-side login
  method and approved pending requests. It does not revoke the actual license.
- Expired, revoked, suspended or blacklisted licenses cannot sign in this way.
- A standard customer's key remains locked to its authorized PC. Discord approval
  does **not** reset or transfer the HWID. Developer unlimited-PC rules remain
  issuer-controlled.
- If locked out, missing the Discord account, or replacing a PC: use the original
  license key and **Request HWID reset**. The authorized operator must review it.
  Keep the key privately; a Discord username alone is not recovery proof.
- Previously linked users must enable this feature once; the server does not
  reconstruct or expose keys from old hashed associations automatically.

## 5. Enroll the owner Host/Master

1. Sign in with the server owner's own Developer-capable license.
2. Link it to the account that is the **current Discord guild owner**.
3. Open **Dev Tools > Server access > 2. Request Host / Master access**.
4. In private **gm-approvals**, the owner sends the exact displayed command:

   ```text
   !admin approve REQUEST_CODE host "Verified owner enrollment"
   ```

5. Wait for the bot's confirmation, then click **3. Verify online access**.
6. Confirm the footer/status says Host-Master and the administration tabs unlock.

The request expires in ten minutes. After the first approved Host, the old shared
Admin/bootstrap credential is disabled for managed administration. Host does not
need to remember that old Admin key. Keep the environment secret configured where
startup requires it; it is not an owner-recovery bypass.

All hosted administration requires fresh online license and Discord checks.
Offline Developer access never grants offline moderation.

## 6. Issue, reset and revoke Alt Staff

Use a **separate Developer license** for a staff member, not the active Host key.

1. Staff signs in on their own PC and links their own Discord account.
2. Staff opens **Server access > 2. Issue / reset Alt Staff Key**.
3. GM reviews the request in private **gm-approvals**:

   ```text
   !admin approve REQUEST_CODE staff "Approved staff duties"
   ```

4. Staff clicks **Verify online access**. The private credential stays in their
   per-host/per-license PC session file; never send it through Discord.

Reset uses the same workflow and replaces/revokes the previous staff credential.
No knowledge of the forgotten Admin key is required.

```text
!admin list
!admin revoke HASHED_MEMBER_ID "Access no longer required"
```

Only the current server owner may run these in **gm-approvals**. MOD/Dev roles
alone are insufficient. After managed adoption, staff bot moderation also needs
an active grant and online verification in the loader within the preceding five
minutes. The owner retains direct Discord recovery authority.

For a verified account-recovery case, GM can use:

```text
!asset accounts
!asset rebind HASHED_MEMBER_ID NEW_DISCORD_ID "Verified recovery reason"
```

Rebind revokes old device grants, admin access and Discord-login enrollment.
The user must re-enroll. This is not a self-service account takeover mechanism.

## 7. Make keys through the loader

**Important:** Host authorization and a Keygen issuer API token are different
credentials. A purchased Developer key cannot issue original-host customer keys.

### A. Original service / Keygen

1. Verify Host/Alt Staff access for the selected original service.
2. Open **Dev Tools > Licenses** and choose **License backend: keygen**.
3. Enter the correct **Keygen Account ID**, **User Policy ID** and **Dev Policy ID**.
   Account/policy IDs identify resources; they are not API tokens.
4. Enter a privately provisioned **Keygen Product/Environment token** that is
   authorized for the intended product/environment. Do not use a customer license
   key, Discord bot token or Alt Staff credential in this field.
5. Click **Save backend settings**. The private token belongs only on an
   authorized issuer workstation, never in distributed EXEs, kits or screenshots.
6. Click **Create key**, supply the customer email and select the tier:
   - `standard`: uses **User Policy ID**.
   - `dev`: lifetime Developer Suite, uses **Dev Policy ID**.
   - `owner`: local owner entitlement; still no automatic hosted Host grant.
7. Copy the new key privately from the result dialog and deliver it securely.
   **Refresh** confirms the issued record.

For the original service, the recognized Developer Suite policy is
`32e89706-4e83-4778-842d-580f0739f7bc`. Its duration and maximum machines must
be unlimited (`null`); the loader rejects incompatible Developer issuance.
That policy's label does not create administrative permission.

The loader's Create key dialog is **not a duration/retail-plan picker**. For a
timed standard Keygen plan, select the appropriate already configured policy in
**User Policy ID** before issuance, or use the Keygen dashboard. Changing display
prices does not change policy durations. Verify the policy before creating a key;
timed plans begin according to issuer policy, not Discord badge text.

### B. Your isolated custom server

1. Export/setup the own-server kit using section 9.
2. Select your custom HTTPS profile and sign in with its seeded Developer key.
3. Before managed enrollment, bootstrap access can unlock initial server setup.
   After enrollment, verify your own Host or approved Alt Staff access.
4. In **Licenses**, choose **custom**. Use **Create key**, email and tier.
5. Send the customer **your HTTPS origin and their custom-server key**.
   They select that origin on the loader sign-in screen.

Custom `dev`/`owner` issuance is lifetime and Developer PCs are unlimited.
The current custom Create key UI does not offer a timed-plan duration selector;
do not advertise a timed entitlement merely because you entered a retail price.
Your keys are not valid on the original service or another host.

### Management buttons

| Control | Purpose |
|---|---|
| Refresh | Reload the selected backend's licenses |
| Create key | Issue through that backend with the selected policy/tier |
| Revoke | Suspend/revoke the selected license; verify the result |
| Enable | Reinstate the selected license where the backend permits |
| Reset HWID | Clear issuer/custom machine association after recovery review; next authorized activation binds it |
| Save backend settings | Save your local backend/account/policy/token configuration |
| Admin key / Save key | Custom bootstrap input before managed adoption; not a replacement for Host/Alt Staff |

Never reset an HWID based solely on a public username or an unsolicited DM.
Confirm the key holder's identity, expected PC and support request first.

## 8. Every Developer function: what it is for

| Page/control | Purpose and limits |
|---|---|
| Server access | Link Discord, request Host/Alt Staff, verify live authority, export kit and switch profiles |
| Live activity | View the selected service's reported loader presence; not remote disk/process access |
| Licenses | Issue/list/revoke/reinstate/reset keys, subject to server and issuer credentials |
| Plan Prices | Load the current six-plan display catalog before editing; Publish updates displayed prices only. Blank means Ask for pricing |
| Checkout | Configure supported hosted payment links and enable checkout. Opening/paying a link does not automatically issue a key; verify fulfillment manually |
| Asset moderation | Review submitted CSVs, approve community content, mark authorized official content, remove hosted uploads and review audit events |
| Announcements & Updates | Publish the selected service's banner/link and version notice. A notice is not a signed EXE/APK update |
| Support Inbox | Refresh tickets, select one, enter a reply and Send reply & close |
| Diagnostics | Review reports explicitly submitted by users; double-click a record for its captured log details |
| Blacklist | Add/remove a selected key, email or HWID block with a reason; this is separate from issuer suspension |
| Screenshots | View user-confirmed loader-window screenshots/notes; this does not capture arbitrary remote desktops |
| Script Protection | Test your own script, select required tier, Lock or Unlock for editing. Force lock skips the testing confirmation only |
| Memory Tools | Advanced authorized process inspection/testing. Developer-only; modifying memory can crash or corrupt software |
| Marketplace | Configure local payment/listing information and external API entries; availability is not payment confirmation or automatic transfer |
| Restart as administrator | Explicit Windows elevation for authorized advanced operations. It can block normal Explorer drag/drop; file pickers remain available |
| DLL Injector (main navigation) | Developer-only advanced local process tooling; use only with permission and compatible test software |
| Downloads & Updates > Developer delivery | Offer authorized files to a target customer/license, optionally HWID-restricted; publish/revoke requires hosted admin authority |

### Files, delivery and data boundaries

- Personal imported files remain local unless the user explicitly shares them.
- Asset uploads are normalized CSV data, limited to 512 KiB per submission.
  Sharing consent allows attributed private Discord staff review, then possible
  publication. Official catalogs and customer submissions remain separate.
- Moderators can remove hosted submissions and bot-exported attachments, not
  unrelated customer files or already downloaded copies.
- Developer delivery verifies checksums and asks the customer before downloading.
  Placement override changes destination routing. Lock delivered file limits
  editing/removal inside the loader; it is not an OS filesystem lock or encryption.
  Configs/updates are staged, not silently executed or installed.
- Script protection deters casual copying; it is not unbreakable DRM. Keep your
  original source and backups privately. Existing protected-file formats remain
  readable for compatibility.
- Paired phone-to-PC MCP handles scoped asset operations, not arbitrary remote
  filesystem access or arbitrary code execution.

### Normal paid workspace

Scripts runs/stops user-selected local scripts. Script Screen hosts their UI/output.
Editor edits local source; AI Assistant requires your own configured provider key.
Tools/Plugins launch configured local tools. Asset Finder manages per-game catalogs.
Map Viewer supports game-provider links and local maps; third-party embedding,
coverage and login restrictions apply. Community provides licensed chat/notices.
Appearance controls theme/layout; Remote handles explicit phone pairing and relay.
Debug shows local activity/errors; Help and Language provide guidance/settings.
None of these pages grants hosted staff privileges.

## 9. Smooth setup for your own server and bot

Use **Server access > Export Developer Suite server + bot setup kit**. Export
requires a fresh online Developer entitlement. Extract privately and read
[`SETUP.txt`](custom-server-setup.txt) plus this manual. The kit is not a cloud
hosting subscription, official credentials or an automatic business setup.

1. Provide your own HTTPS origin, persistent storage, Discord server and bot.
2. Install Python 3.14 and `requirements-server.txt` in a private environment.
3. Create your own bot. Enable Message Content and Server Members intents.
   Grant only documented channel/role/message/moderation permissions; no
   Administrator permission. Put its role above roles it manages.
4. Run `python setup_custom_server.py init`. It writes private setup/recovery
   configuration before changing Discord, provisions matched resources and
   creates your first Developer license. No secrets are printed.
5. If interrupted, fix the reported issue and run `resume`; never reinitialize
   over an existing installation or discard recovery credentials.
6. Read `owner-credentials.private.json` privately. Run `check`, then `run`.
   Route HTTPS to local port 8080 and keep the data directory persistent.
   Run one combined backend/bot deployment against its single SQLite database.
7. Verify `/healthz`, sign in to that host, link Discord and enroll its owner Host.
8. Issue its customer keys, review prices/payment configuration and test with
   an authorized customer before announcing the service.

New settings use `BLACHAMMER_AIO_`: `ADMIN_KEY`, `DATA_DIR`, `DB_PATH`,
`COMMUNITY_BACKEND`, `RELAY_ENABLED`, `RELAY_PROXY_HOPS` and
`RELAY_TRUST_RAILWAY_EDGE`. Bot settings retain the standard `DISCORD_` prefix.
Default relay is disabled in the own-server kit. Proxy trust defaults to zero;
enable one hop only behind an ingress that overwrites forwarded headers and
blocks direct public access to the application port.

## 10. Branding, compatibility and backups

Product: **BlacHammer AIO Loader**. Community/server: **Modz me up**.
New database/configuration names use BlacHammer branding. Existing installation
paths, environment aliases, pairing identifiers, protected-script format and
old service/download URLs are compatibility details, not the product's scope.
Do not blindly rename signing identities, package IDs, old release URLs,
database files or encryption derivation constants. That can strand customers.
Game-specific catalogs/provider names still identify their actual game.

New servers default to `blachammer_aio_licenses.db`. Existing legacy databases
are reused, not replaced with empty storage. Set `BLACHAMMER_AIO_DB_PATH`
explicitly if there is ambiguity. Conflicting old/new environment settings fail
instead of silently choosing a secret or database.

Before any major update:

```text
python setup_custom_server.py backup --destination PRIVATE-NEW-BACKUP.db
```

This creates an exclusive consistent SQLite backup and checks integrity. Separately
back up private configuration, owner credentials, delivery storage and
`discord-login.private.key` from the data directory. That file encrypts enabled
Discord-login credentials; a database-only backup cannot recover them. Restrict
NTFS/server permissions and never attach these files to support or public releases.
For managed hosting, use the provider's persistent-volume backup and retention.
Restore only while both HTTP and bot workers are stopped. Keep last-known-good
source/kit/binaries. Never run two workers against conflicting local/cloud copies.

## 11. Troubleshooting

| Symptom | Action |
|---|---|
| HTTPS required / old localhost address | Select the intended original/custom profile; do not disable HTTPS checks |
| Discord says use private panel | Run `!apply customer` in help-desk, follow your own panel link |
| Already linked to another Discord | GM performs verified account recovery; do not bind by username |
| Discord sign-in not enabled | Sign in with key, link this installation, Enable Discord sign-in |
| Sign-in pending | Send the exact temporary `!login` command in your panel, wait for bot confirmation, then Check approval |
| Multiple enabled keys | Use the hashed ID supplied by the bot; never paste the license key |
| HWID mismatch / replacement PC | Enter the original key, request reset, await authorized operator approval |
| Server moderation locked | Developer access is not staff access; request/approve/Verify online |
| Forgotten Admin key | Use owner-approved Host/Alt Staff recovery; do not create an offline backdoor |
| Keygen creation denied | Verify hosted authority, correct account/product/environment token, and selected policy |
| Developer policy rejected | Verify lifetime duration and unlimited machines; do not substitute a customer policy |
| Price publish denied | Verify online access and load published prices before editing; six plans are required |
| Bot 403 / access failure | Check bot membership, intents, permissions, role hierarchy and host logs without exposing tokens |
| Update signature error | Keep the current binary; never disable signature checks. Retry after hosting/CDN propagation |
| User cannot see all controls | Use the scrollbars, Shift+wheel or keyboard navigation rather than maximizing |

Keep troubleshooting evidence limited to redacted errors, version, selected
server and relevant timestamps. Never publish keys, API tokens, private config,
database backups, Discord-login encryption keys or pairing capabilities.
