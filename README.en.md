<div align="center">

<img src="https://music.http5.cn/logo_full.png" alt="SonaWave" width="360">

# SonaWave

A music player for the library you already own: Navidrome / Subsonic, Emby, Jellyfin, fnOS Music, Audiobookshelf, WebDAV, SMB, Baidu Netdisk and local files.

Android (phone / tablet / TV / car) · Windows · Linux · HarmonyOS

[简体中文](README.md) | English

[Website](https://music.http5.cn/?lang=en) · [Docs](https://music.http5.cn/docs/quickly_start.html) · [Changelog](https://music.http5.cn/changelog.html?lang=en)

</div>

> This repository only hosts release packages and issue reports. It does not contain source code.

## Screenshots

**Desktop**

<p align="center">
  <img src="screenshots/zh/pc-home.jpg" alt="Desktop home" width="49%">
  <img src="screenshots/zh/pc-player.jpg" alt="Desktop player" width="49%">
</p>

**Phone**

<p align="center">
  <img src="screenshots/zh/phone-home.jpg" alt="Phone home" width="24%">
  <img src="screenshots/zh/phone-player.jpg" alt="Phone player" width="24%">
  <img src="screenshots/zh/phone-albums.jpg" alt="Phone albums" width="24%">
  <img src="screenshots/zh/phone-mine.jpg" alt="Phone Me tab" width="24%">
</p>

**Tablet / TV**

<p align="center">
  <img src="screenshots/zh/tablet-home.jpg" alt="Tablet home" width="49%">
  <img src="screenshots/zh/tv-home.jpg" alt="TV home" width="49%">
</p>

## Download

| Source | Link |
|---|---|
| GitHub | <https://github.com/Tlntin/SonaWave-Release/releases/latest> |
| GitCode (faster in mainland China) | <https://gitcode.com/Tlntin/SonaWave-Release/releases> |
| HarmonyOS (Huawei AppGallery) | <https://appgallery.huawei.com/app/detail?id=com.tlntin.sonawave> |

Both repositories host identical files.

### Which file do I need?

**Android (Android 7.0 or later, including Android TV and car units)**

Older Huawei / Honor devices on HarmonyOS 2–4 can install the APK too. On HarmonyOS 5 or later, get the native HarmonyOS app from Huawei AppGallery.

| File | For |
|---|---|
| `SonaWave-<version>-android-arm64-v8a.apk` | Almost all phones, tablets, TVs / boxes and car units. **Pick this one if unsure.** |
| `SonaWave-<version>-android-armeabi-v7a.apk` | Older TV boxes and 32-bit devices (use it if the arm64 build fails with "There was a problem parsing the package") |
| `SonaWave-<version>-android-x86_64.apk` | Android emulators on a PC |

**Windows (Windows 10 / 11, 64-bit)**

| File | Notes |
|---|---|
| `…-windows-x64-full-setup.exe` | **Recommended.** Full playback engine with the best support for DSD, the equalizer and network streams |
| `…-windows-x64-lite-setup.exe` | Less than half the size; plays all common formats, but a few rare formats and network streams work better in the full build |

The installer installs for the current user and does not need administrator rights. Install a new version over the old one to upgrade; settings and libraries are kept.

**Linux (x86_64, glibc 2.35 or later: Ubuntu 22.04+, Debian 12+, Fedora 36+ and similar)**

| File | Notes |
|---|---|
| `SonaWave-<version>-linux-x86_64.AppImage` | **Recommended.** The playback engine (libmpv) and a CJK font are bundled; `chmod +x` it and run, nothing else to install |
| `SonaWave-<version>-linux-amd64.deb` | Debian / Ubuntu. `sudo apt install ./SonaWave-<version>-linux-amd64.deb`; apt installs the system libmpv automatically |

**macOS**: planned (Intel / Apple silicon). **iOS**: not available yet.

### Verify your download

Every release includes `SHA256SUMS.txt`:

```powershell
# Windows PowerShell
Get-FileHash .\SonaWave-<version>-windows-x64-full-setup.exe -Algorithm SHA256
```

```bash
# Linux / macOS
sha256sum -c SHA256SUMS.txt --ignore-missing
```

### Installation notes

- **Windows shows "Windows protected your PC"**: the installer is not code-signed yet. Click "More info" → "Run anyway". Only download from the links above.
- **Android blocks installs from unknown sources**: allow your browser or file manager to install apps when prompted.
- **TV boxes**: copy the APK to a USB drive and install it with the box's file manager, or push it with a sideloading tool.

## Features

- **Many sources**: Navidrome / Subsonic, Emby, Jellyfin, fnOS Music, Audiobookshelf (audiobooks), WebDAV, SMB, Baidu Netdisk and local folders, with multiple sources at once
- **Playback**: lossless and CUE sheets, DSD (dsf / dff) in the Windows Full build; equalizer; exclusive output on Windows; play while caching and offline downloads
- **Lyrics**: synced and word-by-word lyrics, translation; desktop lyrics on PC
- **Discovery**: recommendations based on what you like, search suggestions, listening stats; internet radio
- **Library**: favorites and playlists, M3U / TXT playlist import
- **Every screen**: adaptive layouts for phone, tablet and desktop; remote-control navigation on Android TV and car units; system media controls (Windows media overlay, Android notification / lock screen / Bluetooth)
- English, Simplified Chinese and Traditional Chinese, with a dark mode

## Feature comparison

✅ supported · 🚧 partial · ❌ not yet · — not applicable. The HarmonyOS app is on Huawei AppGallery; the other columns are the Android / Windows / Linux builds released here.

| Sources | HarmonyOS | Android phone / tablet | Android TV / car | Windows | Linux |
|---|:-:|:-:|:-:|:-:|:-:|
| Navidrome / Subsonic, Emby, Jellyfin | ✅ | ✅ | ✅ | ✅ | ✅ |
| fnOS Music | ✅ | ✅ | ✅ | ✅ | ✅ |
| Audiobookshelf | ✅ audiobooks + podcasts | 🚧 audiobooks play as albums; no podcasts | 🚧 same | 🚧 same | 🚧 same |
| WebDAV, SMB (with LAN discovery), Baidu Netdisk, local music | ✅ | ✅ | ✅ | ✅ | ✅ |
| Huawei Drive | ✅ | — | — | — | — |
| Multiple servers, address auto-switch, library sync (incl. incremental sync) | ✅ | ✅ | ✅ | ✅ | ✅ |
| Switching servers saves progress and resumes when you switch back | ✅ | ✅ | ✅ | ✅ | ✅ |
| Multiple music libraries per server | ✅ | ✅ All / one library | ✅ Same | ✅ Same | ✅ Same |

| Playback | HarmonyOS | Android phone / tablet | Android TV / car | Windows | Linux |
|---|:-:|:-:|:-:|:-:|:-:|
| Lossless, CUE tracks, equalizer, ReplayGain, fade, sleep timer | ✅ | ✅ | ✅ | ✅ | ✅ |
| DSD (dsf / dff) | ✅ experimental | not verified | not verified | ✅ Full build | not verified |
| Exclusive output | ✅ USB DAC | ❌ | ❌ | ✅ WASAPI | ❌ |
| Play while downloading, offline downloads | ✅ | ✅ | ✅ | ✅ | ✅ |
| Pause / resume downloads, cache to download, import downloaded files | ✅ | ✅ | ✅ | ✅ | ✅ |
| Server-side transcoding | ✅ | ✅ | ✅ | ✅ | ✅ |
| Playback speed | ✅ audiobook mode | ❌ | ❌ | ❌ | ❌ |
| Internet radio | ✅ | ✅ | 🚧 file import / export needs a file manager on the device | ✅ | ✅ |

| Lyrics | HarmonyOS | Android phone / tablet | Android TV / car | Windows | Linux |
|---|:-:|:-:|:-:|:-:|:-:|
| Synced & word-by-word lyrics, translation, editing | ✅ | ✅ | ✅ | ✅ | ✅ |
| Embedded / same-name .lrc lyrics and covers (local, SMB, WebDAV) | ✅ | ✅ | ✅ | ✅ | ✅ |
| Per-line timing calibration | ✅ | 🚧 global offset only | 🚧 same | 🚧 same | 🚧 same |
| Desktop / floating lyrics | ✅ | ✅ floating lyrics | ❌ | ✅ | ✅ |
| Car Bluetooth lyrics | ✅ | ✅ | ✅ | — | — |

| Library & playlists | HarmonyOS | Android phone / tablet | Android TV / car | Windows | Linux |
|---|:-:|:-:|:-:|:-:|:-:|
| Smart home page, search suggestions, favorites, multi-select, listening stats | ✅ | ✅ | ✅ | ✅ | ✅ |
| Folder browsing | ✅ | 🚧 not for Audiobookshelf | 🚧 same | 🚧 same | 🚧 same |
| Playlist from a folder (add a whole folder to a playlist / favorites / queue) | ✅ | 🚧 not for Audiobookshelf; playlists only on server sources | 🚧 same | 🚧 same | 🚧 same |
| Folder management (create / rename / move / delete) | ✅ | ✅ local / SMB / WebDAV / Baidu Netdisk | ✅ same | ✅ same | ✅ same |
| Playlists: create, add songs, delete, import | ✅ | ✅ | ✅ import needs a file manager on the device | ✅ | ✅ |
| Playlists: rename, reorder, remove songs, export / share | ✅ | ✅ | ✅ | ✅ | ✅ |
| Edit song info / cover / lyrics | ✅ | ✅ local MP3 / FLAC can be written into the file, or saved as sidecar files | ✅ same | ✅ same | ✅ same |
| Hide video-only Emby / Jellyfin playlists | ✅ | ✅ | ✅ | ✅ | ✅ |
| Metadata fill (batch covers / lyrics) | ✅ | ✅ | ✅ | ✅ | ✅ |
| Similar songs | ✅ | 🚧 Navidrome / Subsonic, Emby, Jellyfin | 🚧 same | 🚧 same | 🚧 same |
| Automatic backup & restore of playlists / favorites / radio | ✅ | ✅ | ✅ | ✅ | ✅ |
| Upload to cloud drive | ✅ Huawei Drive / Baidu Netdisk | ✅ Baidu Netdisk | ✅ Baidu Netdisk | ✅ Baidu Netdisk | ✅ Baidu Netdisk |
| Choose the default cover (separate for music and radio, or use your own image) | 🚧 one fixed image | ✅ | ✅ | ✅ | ✅ |
| Queue history | ✅ | ✅ | ✅ | ✅ | ✅ |
| Audiobook mode (bookshelf, resume, speed), book store | ✅ | ❌ | ❌ | ❌ | ❌ |

| System & account | HarmonyOS | Android phone / tablet | Android TV / car | Windows | Linux |
|---|:-:|:-:|:-:|:-:|:-:|
| System media controls (notification / lock screen / headset keys / media overlay) | ✅ | ✅ | ✅ | ✅ | ✅ |
| Cross-device continuation, casting | ✅ | ❌ | ❌ | ❌ | ❌ |
| Remote-control navigation; switch between tablet and TV layouts | — | ✅ switchable | ✅ | — | — |
| Tray, shortcuts, drag-and-drop | — | — | — | ✅ | ✅ |
| Open with (open files from the file manager) | ✅ | ✅ incl. audio / m3u shared from other apps | ✅ needs a file manager on the device | ✅ | ❌ |
| Android Auto | — | — | 🚧 browse, pick songs, voice search; not yet tested in a real car | — | — |
| Sign-in | ✅ Huawei ID | ✅ email / QR | ✅ email / QR | ✅ email / QR | ✅ email / QR |
| Membership (shared across platforms) | ✅ Huawei IAP | ✅ Alipay | ✅ Alipay | ✅ Alipay | ✅ Alipay |
| Themes, accent colors, dark mode, 3 languages | ✅ | ✅ | ✅ | ✅ | ✅ |
| Export / import settings | ✅ | ✅ | 🚧 needs a file manager on the device | ✅ | ✅ |

## Feedback

Found a bug or have an idea? Open an [issue](../../issues) and include:

- Your OS and device (for example Windows 11, Pixel 8, Chromecast with Google TV)
- The app version (Me → About)
- Your source type (Navidrome, Emby, SMB…)
- Steps to reproduce, ideally with a screenshot

**Never post server addresses, passwords or tokens in an issue.**

### Sending debug logs

For playback or connection problems, a debug log helps a lot:

1. Go to Me → Settings (top right) → Advanced Settings → Debug logs, and turn on "Record debug logs".
2. **Without restarting the app**, repeat whatever went wrong.
3. Go back to Debug logs and tap Copy (top right).
4. Paste the log into an email to **tlntindeng01@gmail.com**, and mention "log sent by email" in your issue.

Passwords and tokens are masked automatically, but the log still contains your server address, so **please don't paste it into a public issue**. Only logs since the current launch are kept; you can turn recording off when you're done.

## Legal

- [Terms of Service](https://music.http5.cn/flutter-terms.html?lang=en)
- [Privacy Policy](https://music.http5.cn/flutter-privacy.html?lang=en)
- [Membership Agreement](https://music.http5.cn/flutter-member.html?lang=en)
