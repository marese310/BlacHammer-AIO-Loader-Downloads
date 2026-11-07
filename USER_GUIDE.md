# BlacHammer AIO Loader - Getting Started

For **Windows loader 4.2.0** and **Android Companion 3.2.0**.
Created by **BlacHammer**. Community: [Modz me up](https://discord.gg/qeGAX6VCUz).

**New here? Follow sections 1-4 first. You do not need to build anything.**

## 1. Download the right files

Use the [official downloads](https://github.com/marese310/BlacHammer-AIO-Loader-Downloads/releases/latest).

| Your device | Download | What it does |
|---|---|---|
| Windows PC | `BlacHammerAIOLoader_v4.2.0.exe` | The main loader. Keep it running for phone control. |
| Android phone | `BlacHammerAIOLoaderCompanion_v3.2.0.apk` | The companion; it does not replace the Windows loader. |

1. Make a folder such as `Documents\BlacHammer AIO Loader`.
2. Put the EXE there and double-click it. No Python installation is needed to
   open the official EXE. Python scripts you run may need Python separately.
3. Windows may show an unsigned-app/SmartScreen warning. Do not disable your
   antivirus. Verify the download source first; ask support if uncertain.
   The release's `SHA256SUMS.txt` can be used to check the downloaded file.
4. On Android, open the APK. If necessary, allow installation from the browser
   you used, install, then turn that permission back off.
5. **Updating? Install over the existing Android app. Do not uninstall or clear
   its data**, or you may lose pairing and saved settings.

Do not download a developer source package for normal use.

## 2. Choose Free or activate your key

- **Continue Free**: Asset Finder and Map Viewer only; no key is needed.
- **Paid**: obtain your own license key from BlacHammer/an authorized seller,
  enter it on the sign-in screen and choose **Sign in**.
- Use the **original server** for an official key. Choose a custom server only
  when its operator has given you its address and a key for that server.

Keep your key somewhere private. Never post it in a public channel, screenshot
or support message. A normal license can have a PC/device limit. Ask the owner
for an authorized HWID reset when changing computers; Discord login cannot
bypass that limit.

Developer features require an owner-issued Developer license. Buying Developer
Suite does not make someone a GM, Host or staff member.

If a license expires or is revoked, paid access stops and the loader may close.
Reopen it and choose Free to use the free features. It does not silently convert
an active paid session into Free.

## 3. Find your way around

The left navigation chooses a page. The search box helps find pages.
Use **Dashboard** to return home. In a smaller window, use the right scrollbar
and bottom scrollbar; Shift + mouse wheel scrolls sideways. Use Tab to move
between controls.

| Page | Use it for |
|---|---|
| Asset Finder | Search game asset data; select/import a separate game library. |
| Map Viewer | View your maps or open supported map websites. Websites may need their own login. |
| Scripts | Add, run and stop scripts you trust. |
| Script Screen | View supported script GUI windows; release a GUI to its own window if needed. |
| Tools | Register and launch programs such as EXE/BAT/CMD files. |
| Plugins | Register resources/DLL/config files and choose a compatible launcher. |
| Editor / AI Assistant | Edit scripts; AI features may need separately configured service access. Do not send secrets. |
| Community | Browse/download the available community scripts. A listing is not a safety guarantee. |
| Remote | Pair your phone and explicitly approve optional screen viewing/input. |
| Debug / Output | See loader messages and captured output from programs it started. |
| Help / Account & Support | Read help, manage sign-in or request assistance. |
| Dev Tools | Licensed Developer features; hosted administration needs separate verified permission. |

Some pages are hidden or locked in Free mode. That is expected, not a fault.

## 4. Add and run your first trusted file

**Only run files you own or have permission to use and trust. Scripts run with
your Windows permissions; they are not sandboxed or automatically safety-approved.**

### A script

1. Open **Scripts** and add your script files/folder, or drag a script into the loader.
2. Read and confirm the drop summary. Dropping does not run the file.
3. Click the file's row once to select it. Use its run control, or double-click
   the actual file row to run it.
4. Check its status and output. Use **Stop** when finished.
5. Only enter **Arguments** if the script author supplied instructions.
   Arguments are extra startup options, not a license key field.

### A normal program

1. Open **Tools > Add tool**, choose the program, and give it a recognizable name.
2. Leave optional arguments blank unless you know they are needed.
3. Select it and click **Start**, or double-click its row.
4. Use **Output** for captured text and **Stop** to end the tracked program.
   Save work first; stopping a program may discard unsaved changes.

You can run several registered tools and scripts. Programs with their own GUI
can keep separate windows. In Scripts, **Release GUI to its own window** leaves
the program running rather than stopping it.

### What happens when you drag in different files?

| File | Where it goes |
|---|---|
| Python/protected scripts or script folders | Scripts |
| EXE/COM/BAT/CMD | Tools |
| CSV asset data | A separate asset library |
| DLL/config/other regular files | Plugins/resources |

The loader registers originals **where they already are**. It does not move,
silently upload, automatically run or inject them. Keep those folders available.
In Plugins, **Set launcher** chooses a program that knows how to open the resource.
A DLL is not a normal standalone program. Unknown resources open their folder
until you explicitly choose a compatible launcher.

If a tool renames itself in the **same folder and extension**, the loader tries
to recognize it. If it cannot identify one safe match, choose **Relink file**
and select the correct file yourself. Moving it to another folder needs relinking.

## 5. Use your Android phone

### Pair once

1. Leave the Windows loader running and signed in with an active paid license.
2. Open **Remote**, enable Remote, and choose your connection:
   - **Internet relay**: both devices need Internet; no router port forwarding.
   - **LAN / private VPN**: both devices must be able to reach the PC.
   - **Bluetooth**: use the app's supported secure pairing flow and OS permissions.
3. Open **Scan-to-pair QR** on the PC.
4. On the phone, open **Pair PC**, scan the fresh PC QR or paste its setup link,
   then choose the matching connection type.
5. Check the phone name on your PC and approve **your own phone**.
6. Open the phone **Dashboard**. It should show your PC and running programs.

Treat QR/setup links like private passwords. Never post them or open a public
router port to fix pairing. Keep the PC awake. Revoke a lost/unrecognized phone
from PC Remote.

### Watch and control

- Open a running script's log on the phone to see its captured output.
  Input works only if that running script actually reads standard input.
- For a GUI, close sensitive PC windows first. On PC **Remote**, explicitly
  approve screen sharing. Approve input separately only if you need control.
- On the phone, open **Portable workspace**. Enable its input checkbox to
  send taps, short text, navigation keys or scrolling to the active PC window.
- **Warning: PC approval covers all currently paired phones**, not just the
  phone you are holding. It lasts ten minutes.
- Use **STOP PC sharing and input** on the phone or stop sharing on the PC.
  Leaving the phone page clears its preview/input checkbox but does not stop scripts.

Preview is a management aid: **up to 960x540, one frame per second**, not smooth
gameplay streaming. There is no audio/gamepad forwarding or UAC/secure-window
bypass. Slow frames do not necessarily mean the program has stopped.

## 6. Sign in with Discord after linking

1. Sign in with your key first.
2. Open **Asset Finder > Shared Asset Hub > Link Discord**.
3. Send the displayed `!asset link CODE` in **your own private customer panel**
   in Modz me up. Ask staff for a panel if you do not have one.
4. Return to the hub and choose **Enable Discord sign-in**.
5. Next time, choose **Sign in with Discord**, send the displayed `!login CODE`
   in your private panel, and click **Check approval** on your PC.

Only approve a code from your own current sign-in attempt. Do not send your key
or Discord password. Keep the key for recovery and HWID resets. The license must
still be valid; Discord linking is not free paid access.

## 7. Private files versus sharing

Adding a local script/tool **does not submit its code to GMs**. Script submission,
private code review and approve-before-public-release are **planned for the next
update, not available in 4.2.0**. Do not assume a script has been inspected.

The current **Shared Asset Hub** is for CSV asset data, not script code. Its
explicit upload consent sends a normalized copy and your Discord attribution to
private staff review. Approved CSVs may then be published to customers.
Do not include secrets or personal data. Imported/private libraries are not
silently uploaded. Staff removal cannot erase copies people already downloaded.

## 8. Common problems

| Problem | Try this |
|---|---|
| Missing paid pages | Check edition/sign-in. Free intentionally has fewer pages. |
| Unknown key | Check original/custom server, spelling and license status with the issuer. Never paste the key publicly. |
| HWID/device limit | Ask BlacHammer for an authorized reset; keep your original key. |
| Script cannot find Python or a package | Follow that script author's Python/dependency instructions. The loader EXE's bundled Python is not your general script environment. |
| Tool file disappeared | Keep the original folder; use Relink file if recognition fails. |
| No useful error in Output | Some GUIs do not write text output. Check that program's own logs; the loader does not inspect every Windows application's errors. |
| Phone cannot connect | Keep PC awake, check Remote/relay state and network, then try a fresh QR and approve the named phone. Do not disable TLS checks. |
| Preview/input unavailable | Update both apps, reapprove PC sharing/input, enable the phone checkbox and refresh. Elevated/protected windows may not work. |
| APK update refuses to install | Use the official APK with the matching signer. Ask support before uninstalling and losing data. |
| Cannot see a button | Scroll right/down or use Tab instead of repeatedly enlarging the window. |

For help, send your app versions, what you clicked and the exact error with
keys, QR codes, tokens and personal information removed. Press **F1** for support.
Use **Check version** in the footer to verify the signed official update feed.

Advanced controls: [Developer and Host Manual](DEV_TOOLS_README.md).
