# VoltSender — Free Wi-Fi File Transfer Between PC and Phone (No App Install)

**Send files between PC and phone — or between two PCs — over your local Wi-Fi in seconds. No cable, no cloud, no accounts, no ads. The receiving device just needs a browser.**

VoltSender is a free file transfer app for Windows 10 and Windows 11 that turns your PC into a private local server. Point your phone camera at the QR code (or open the link on another PC), tap the link, and share photos, videos, PDFs, ZIPs, or plain text back and forth at full Wi-Fi speed. Everything stays on your network — no data ever touches a cloud provider.

Think of it as an AirDrop-style file transfer for Windows that works with **any** device — Android phone, iPhone, iPad, tablet, another Windows PC, a Mac, a Linux laptop, or a Chromebook — because the client side is just a webpage.

![VoltSender main window on Windows 11 showing a QR code, Wi-Fi network status, and file transfer panels for sending and receiving files between PC and phone](https://github.com/user-attachments/assets/2333b23d-cf2d-4f06-9909-b41ce9a1e8fe)

---

## Download

- **Latest release (Windows x64):** [download the installer](#) *(link once you publish releases)*
- **SHA-256 checksum:** listed on the release page — verify with `certutil -hashfile VoltSender-Setup.exe SHA256`
- **Source code:** [GitHub repository](#) *(link once public)*

VoltSender is **100% free** and always will be. No paid tier, no subscription, no telemetry, no watermark, no file-size limit imposed by us.

---

## Quick Start (60 seconds)

1. **Install and launch** VoltSender on your Windows PC.
2. **Show the QR code** — it appears automatically on the left card, along with a link like `http://192.168.1.42:5678`.
3. **Open your phone camera** and point it at the QR code. Tap the notification that pops up. Your phone browser opens the VoltSender web app. *(On another PC on the same Wi-Fi, just paste the URL into any browser instead.)*
4. **Send or receive.** Drag files onto the PC window to send them to the other device. On the phone or second PC, tap "Send" to pick files and push them back.

Received files land in `Documents\VoltSender` by default (change it under Settings). If Auto-organize is on, they get sorted into `Photos`, `Videos`, `Documents`, `Audio`, `Archives`, and `Other` subfolders.

---

## Why VoltSender

| | VoltSender | Cloud services (Drive, Dropbox…) | AirDrop | USB cable |
|---|---|---|---|---|
| Works PC ↔ phone | Yes | Yes | Apple-only | Yes but slow |
| Works PC ↔ PC on same Wi-Fi | **Yes** | Yes | Apple-only | No |
| Requires client-side install | **No** (browser only) | Yes | Yes | Sometimes |
| Requires account / sign-in | **No** | Yes | Yes | No |
| Works with no internet | **Yes** (LAN only) | No | Yes | Yes |
| File-size cap | **None** | Free-tier caps | ~4 GB practical | None |
| Files leave your network | **Never** | Always | Never | Never |
| Free forever | **Yes** | Free tier | Yes | Yes |

VoltSender is designed for people who want the **speed and privacy of a direct connection**, without the friction of pairing, installing companion apps, or trusting a third-party cloud with their files.

---

## Screenshots

### On your Windows PC

<p align="center">
  <img src="https://github.com/user-attachments/assets/d57d2524-b350-406e-926b-4dde28a93901" width="460" alt="VoltSender Settings window on Windows — receive folder, transfer chunk size, launch-at-startup, theme, and About panel">
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/b5d04d85-3cd9-4821-acca-1e1c84f4acc7" width="460" alt="VoltSender animated splash screen at app launch — brand mark with cyan and electric-blue accents on a deep navy background">
</p>

<p align="center"><sub><b>Left:</b> Settings — receive folder, chunk size, startup, and theme. &nbsp;·&nbsp; <b>Right:</b> Launch splash.</sub></p>

### On any client — phone, tablet, or second PC

The client side is a webpage — no app to install. Works with Chrome, Safari, Firefox, Edge, Samsung Internet, and any modern browser on Android, iOS, iPadOS, Windows, macOS, Linux, or ChromeOS.

<table align="center">
  <tr>
    <td align="center" width="33%">
      <img src="https://github.com/user-attachments/assets/0cba24aa-96cf-4712-b985-2adf95673f68" width="260" alt="VoltSender phone web app on Android Chrome — connected status, live PC device name, and file transfer entry point">
      <br><sub><b>Connected to PC</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="https://github.com/user-attachments/assets/aeb858fe-9acf-4e62-a029-f44f6de5fc26" width="260" alt="Sending files from Android phone to Windows PC via VoltSender — file picker with chunked upload progress">
      <br><sub><b>Send phone → PC</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="https://github.com/user-attachments/assets/08d1716c-89c7-4b6a-a3aa-a7be3f11d929" width="260" alt="Received files list in VoltSender phone browser — download files shared from Windows PC over Wi-Fi">
      <br><sub><b>Receive PC → phone</b></sub>
    </td>
  </tr>
</table>

---

## Features

### File transfer

- **PC to phone** — click *Add files* or drag & drop onto the window. The phone gets an instant download list.
- **Phone to PC** — pick files from the phone's Send tab. They stream directly to your PC with real-time progress and speed indicators.
- **PC to PC** — open the QR link in a browser on any other PC on the same Wi-Fi. Same UI, same speeds, same resumable transfers — no second install needed on the receiving machine.
- **Resumable uploads** — if the Wi-Fi drops mid-transfer, VoltSender retries the current chunk and continues from where it left off. A large upload never restarts from zero.
- **Any file, any size** — 4K videos, RAW photos, ISO images, ZIP archives, source code. VoltSender does not inspect or process file contents.
- **Range-based downloads** — the client browser can pause and resume downloads of large files thanks to HTTP range support.

### Text and clipboard sharing

- **Send text snippets, URLs, or clipboard contents** between phone and PC. Handy for pasting a link you copied on your phone into your PC browser, or sharing a Wi-Fi password.
- Text history is stored in memory only (up to the 50 most recent snippets) and cleared when the app closes.

### Multiple devices

- Multiple phones, tablets, or PCs can connect at the same time. Each device sees its own send/receive view.
- The host PC shows a live device list with connection time and IP.

### Reliability

- **Auto-organize incoming files** into Photos / Videos / Documents / Audio / Archives / Other subfolders (toggle in Settings).
- **Fresh port per session** — VoltSender picks an unused network port each launch, so it works even if another app is already using a common port.
- **Retries on port collision** — if the first port fails, it automatically tries additional ones before showing an error.
- **Rolling log file** at `%LocalAppData%\VoltSender\logs\` for diagnosing rare issues. Kept for 7 days, then auto-cleaned.
- **Global crash handler** — if something goes wrong, you get a clear dialog with an "Open logs" button instead of a silent crash.

### Convenience

- **Tray icon** — close the window and VoltSender keeps running in the notification area so your phone can still connect.
- **Launch at startup** (optional) — enable in Settings for one-tap access every time you boot.
- **Single-instance** — only one copy of VoltSender ever runs, so tapping the icon twice never opens duplicate windows.
- **High-DPI ready** — sharp on 4K, ultrawide, and mixed-DPI multi-monitor setups.
- **Segoe Fluent Icons** — matches the Windows 11 visual style; falls back to Segoe MDL2 Assets on Windows 10.

---

## Installation Guide

### Step 1 — Download

Grab `VoltSender-Setup.exe` from the [releases page](#).

### Step 2 — Handle the SmartScreen prompt (first download only)

Because VoltSender is a small independent project without a paid Authenticode code-signing certificate, Windows SmartScreen may show a blue "Windows protected your PC" screen the first time you run the installer. This is standard for new publishers.

**To run it:**
1. Click **More info**.
2. Click **Run anyway**.

You can also verify the file integrity yourself before running it:
```
certutil -hashfile VoltSender-Setup.exe SHA256
```
Compare the output with the SHA-256 published on the release page. If they match, the download was not tampered with.

### Step 3 — Install

Run the installer and follow the wizard. VoltSender installs to `C:\Program Files\VoltSender\` by default and adds:
- A Start Menu entry
- An optional desktop shortcut
- A Windows Firewall allow-rule on Private networks (auto)
- An Add/Remove Programs entry for clean uninstall

### Step 4 — Allow through Windows Firewall

The first time you launch VoltSender, Windows may show a Firewall dialog asking whether to allow VoltSender on Private or Public networks.

**Check the "Private networks" box and click Allow Access.** This lets your phone reach the PC over your home Wi-Fi. Leave "Public networks" unchecked — that's for airports, coffee shops, and other untrusted networks.

If you miss the prompt, you can fix it later in **Windows Security → Firewall & network protection → Allow an app through firewall → VoltSender → check Private**.

---

## System Requirements

| Component | Requirement |
|---|---|
| Operating system | Windows 10 (version 1809 or later) or Windows 11, 64-bit |
| .NET runtime | Bundled in the installer — no separate .NET download needed |
| Disk space | ~80 MB for the app; plus whatever you receive |
| Network | Any Wi-Fi or Ethernet LAN that both devices share |
| Client device | Any modern browser: Chrome, Safari, Firefox, Edge, Samsung Internet, Brave |
| Client OS | Android 8+, iOS 13+, iPadOS 13+, HarmonyOS, Windows, macOS, Linux, ChromeOS — anything with a browser |

VoltSender does **not** require an internet connection to work. If your Wi-Fi router has no internet uplink, transfers still work over the LAN at full speed.

---

## How to Use — Detailed

### Connecting your phone

1. Make sure your phone and PC are on the **same Wi-Fi network** (or connected to the same router via Wi-Fi/Ethernet).
2. Launch VoltSender. Wait a second for the QR code to render.
3. Open your phone camera app. Point it at the QR code on the PC. A link banner appears — tap it.
4. Your phone browser opens the VoltSender web page. The PC status pill turns green and says "Phone connected".

If the camera doesn't recognize the QR (rare — usually poor lighting or screen glare), you can also type the URL shown under the QR into any browser on the phone.

### Sending files from PC to phone

1. On the PC, click **Add files** in the "Send to phone" card. Multi-select is supported.
2. Or **drag files or folders** directly onto the VoltSender window.
3. On the phone, the files appear in a list. Tap any file to download, or turn on auto-download to grab everything as it arrives.

### Sending files from phone to PC

1. On the phone browser, tap **Send** or drag-drop files onto the phone page.
2. Files upload in chunks with a live progress bar.
3. When done, they appear in the PC's "Received from phone" list and land in the receive folder (default: `Documents\VoltSender`).

### Sending files between two PCs (PC-to-PC transfer)

VoltSender doubles as a PC-to-PC file transfer tool on your local Wi-Fi. You only need to install VoltSender on the **host** PC (the one holding or receiving the files) — the second PC just needs a browser.

1. On the **host PC**, launch VoltSender and note the URL under the QR code (e.g. `http://192.168.1.42:5678`).
2. On the **second PC**, open any browser and paste that URL into the address bar.
3. The same web app that phones see now opens on the second PC. Use **Send** to upload files from the second PC to the host, or the **Files** list to download files the host is sharing.
4. Transfers use the same resumable, chunked protocol — so a big folder-worth of files survives a Wi-Fi hiccup.

This is handy for moving files between a laptop and desktop, off an old PC before decommissioning it, or between two computers in the same room without hunting for a USB drive.

### Sharing text or clipboard snippets

1. Switch to the **Text** sub-tab on the PC's "Received from phone" card (or on the phone).
2. Type or paste text, then hit **Send** (or press Enter).
3. The other side sees it immediately. Click a snippet to copy it back to your clipboard.

Perfect for sharing a Wi-Fi password, a long URL, an OTP code, or a snippet of text you don't want to retype.

### Managing received files

- Click **Open folder** on the PC to jump to your receive folder in Explorer.
- Right-click any received item for **Open**, **Show in folder**, or **Delete**.
- Change the receive folder location under **Settings → Receive folder**.

---

## Privacy and Security

VoltSender was built with a "**your files are your business**" philosophy. Concretely:

- **Fully offline transfer.** Every byte travels directly between your PC and your phone over the same Wi-Fi. Nothing is uploaded to any cloud, and VoltSender itself makes no outbound internet requests.
- **No accounts.** You do not need to sign up, sign in, or provide an email.
- **No telemetry, no analytics, no ads.** VoltSender does not phone home. Ever.
- **No data collection.** VoltSender does not read, index, or process your files. It only moves the bytes.
- **Local server only.** The embedded Kestrel web server binds to your local network interfaces. It is not reachable from the internet unless you explicitly punch a hole through your router (don't).
- **Auto-organize is local.** File classification happens on your PC using file extensions — no content is sent anywhere.
- **Logs stay local.** The rolling log file at `%LocalAppData%\VoltSender\logs\` is on your PC only. You choose what to share when reporting a bug.

### Security notes

- **Trust your Wi-Fi.** Anyone on the same local network could reach the server while it is running. On your home Wi-Fi this is you and your household. On guest/public Wi-Fi (hotels, cafes), other devices could theoretically discover it. **Do not run VoltSender on untrusted networks** unless you are OK with anyone on that network being able to send you files.
- **HTTPS/TLS.** VoltSender uses plain HTTP over the LAN. This is fine for private networks. If you need cryptographic protection on hostile networks, use a Wi-Fi hotspot from your phone instead.
- **File-size cap on text.** Text snippets are capped at 32 KB to prevent memory abuse. Files themselves have no cap.

---

## Troubleshooting and FAQ

### The QR code appears but my phone can't connect after scanning

Most common cause: the phone is on a different Wi-Fi than the PC. Cellular data is off but the phone remembered a different network. Fix:

1. On the phone, open **Settings → Wi-Fi** and confirm you are on the **same network name** shown on the PC's Wi-Fi card.
2. Some routers isolate wireless clients from each other ("AP isolation" or "guest network mode"). Disable it in the router admin panel, or connect both devices to the main SSID rather than the guest one.
3. Corporate / hotel / airport Wi-Fi frequently blocks device-to-device traffic on purpose. Use a phone hotspot instead in that case.

### VoltSender says "Couldn't start"

The Kestrel server couldn't bind to a network port. Usually:

1. **Windows Firewall blocked it.** Click **Yes** to retry, and this time answer **Allow** with Private networks checked.
2. **Antivirus is blocking local sockets.** Add VoltSender to your antivirus's allow list.
3. **Something else is holding the port.** VoltSender automatically retries with fresh ports, so this is rare. Reboot if it keeps happening.

The failure dialog offers an **Open log folder** button — the log tells you exactly which port failed and why.

### Transfers are slow

Speed depends on the weakest link between the two devices:

- Are both devices on **5 GHz Wi-Fi**? 2.4 GHz caps out around 15 MB/s in practice.
- Is the PC on Ethernet and the phone on Wi-Fi 6? That's the fastest combo.
- Router load — many cheap routers slow down when several devices are active.
- Antivirus real-time scanning on the receive folder can slow writes. Exclude the receive folder if needed.
- If speed is still poor, try increasing **chunk size** in Settings from 4 MB to 8 MB.

### Does VoltSender work with iPhone / iPad?

**Yes.** The phone side is a webpage — it works with Safari, Chrome, and every modern iOS/iPadOS browser. iCloud Photos and Files integration works too: tap the file picker and choose from iCloud Drive or your Camera Roll.

### Does VoltSender work with Android?

**Yes.** Chrome, Firefox, Samsung Internet, Brave, Edge — all supported. Android's built-in file picker gives you access to Downloads, Google Drive, Photos, and any DocumentsProvider app.

### Can I transfer files between two PCs (PC to PC)?

**Yes.** Install VoltSender on one PC (the host), then on any other PC on the same Wi-Fi just open the URL shown under the QR code in any browser. No second install needed. This works for Windows-to-Windows, Windows-to-Mac, Windows-to-Linux, and Windows-to-Chromebook — anything with a browser.

### Does VoltSender work with Mac, Linux, or Chromebook?

**As a client, yes.** The host must be a Windows PC (that's where VoltSender runs), but any Mac, Linux machine, or Chromebook on the same Wi-Fi can connect through its browser and send/receive files. A native macOS/Linux host build is not currently available.

### Does it work over mobile data / cellular?

**No, by design.** VoltSender is LAN-only. If you need to transfer files across the internet, use a cloud service instead — it's a different use case.

### Can I use it on a work network?

Only if IT allows peer-to-peer traffic. Many corporate networks block it. Test with a small file first.

### What ports does VoltSender use?

VoltSender picks a fresh port each launch (any free port above 1024). Nothing is hardcoded. This is why it rarely conflicts with anything.

### Where are received files saved?

Default: `Documents\VoltSender`. Change it under **Settings → Receive folder**. With Auto-organize on, files go into subfolders by type.

### Can I keep VoltSender running in the background?

**Yes.** Closing the window minimizes to the system tray. Right-click the tray icon for **Show**, **Guide**, or **Quit**. Enable **Launch at startup** in Settings to have it always available.

### How do I uninstall?

**Settings → Apps → Installed apps → VoltSender → Uninstall.** VoltSender leaves the receive folder alone (that's your files). To fully remove settings + logs, delete `%LocalAppData%\VoltSender\` afterward.

### Is VoltSender open source?

The source is [available on GitHub](#) — feel free to inspect it, fork it, or contribute.

### How does VoltSender make money?

**It doesn't.** VoltSender is a free project. If you find it useful, star the repo or tell a friend.

---

## Advanced Settings

Open **Settings** from the header.

| Setting | Default | Notes |
|---|---|---|
| Receive folder | `Documents\VoltSender` | Any folder you have write access to |
| Auto-organize | On | Sorts into Photos / Videos / Documents / Audio / Archives / Other |
| Auto-download by default | On | Hint for the phone UI on first load |
| Chunk size | 4 MB | 2 MB for weak Wi-Fi, 8 MB for fast Wi-Fi |
| Launch at startup | Off | Runs quietly in the system tray |
| Theme | System | Light or Dark (Dark coming soon) |

Settings persist to `%LocalAppData%\VoltSender\settings.json`.

---

## Keyboard Shortcuts

| Key | Action |
|---|---|
| Enter | Send the text snippet in the Text tab |
| Esc | Close the Guide overlay |

---

## Reporting Bugs

1. Reproduce the issue.
2. Open **Settings** to find the log folder path (or navigate to `%LocalAppData%\VoltSender\logs\`).
3. Grab the most recent `voltsender-YYYYMMDD.log` file.
4. Open a [GitHub issue](#) with:
   - What you tried to do
   - What happened instead
   - The log file (attach it — never paste it inline, logs may contain filenames)
   - Windows version (`winver`)

The log file contains **no file contents**, only filenames, sizes, timestamps, and error messages.

---

## Roadmap

Planned for future versions:

- Dark theme
- Optional PIN protection for the LAN server
- Self-signed TLS for encrypted transfers on hostile networks
- MSIX distribution via the Microsoft Store
- Auto-update

Feedback welcome via the [issues page](#).

---

## License

VoltSender is released under the **MIT License**. You can use it for personal or commercial purposes at no cost. See [LICENSE](LICENSE) for the full text.

---

## Credits

- **VoltSender** by MediaByteX
- Built with **.NET 6 / WPF** and **ASP.NET Core Kestrel**
- QR generation via [QRCoder](https://github.com/codebude/QRCoder)
- Icons: **Segoe Fluent Icons** (Windows 11) / **Segoe MDL2 Assets** (Windows 10)

---

## Related Searches

*(For search engines and users landing here from Google, Bing, or DuckDuckGo.)*

VoltSender is often searched as: **Wi-Fi file transfer for Windows**, **PC to phone file share**, **phone to PC file transfer no cable**, **PC to PC file transfer over Wi-Fi**, **transfer files between two computers on same network**, **laptop to desktop file transfer wireless**, **AirDrop alternative for Windows**, **wireless file transfer app**, **local network file share Windows 11**, **QR code file transfer**, **send files from PC to Android without USB**, **iPhone to Windows file transfer over Wi-Fi**, **Windows to Mac file transfer local**, **free file share app no cloud**, **LAN file transfer software**, **browser-based file sharing**, **peer-to-peer file transfer Windows**, **share files across devices same Wi-Fi**, **no-account file transfer**, **offline file transfer**.

If you found this project via one of those, welcome — that's exactly what VoltSender does.
