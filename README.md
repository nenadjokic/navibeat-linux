<div align="center">

<img src="docs/img/logo.png" alt="NaviBeat" width="108" height="108">

# NaviBeat for Linux

**A native desktop music player for your own Navidrome or OpenSubsonic server.**

Part of the NaviBeat ecosystem. This build is for **Linux only**. For the Apple ecosystem, see the [App Store links](#part-of-the-navibeat-ecosystem) below.

[Download](#download) &nbsp;&middot;&nbsp; [Features](#features) &nbsp;&middot;&nbsp; [Install](#install) &nbsp;&middot;&nbsp; [Website](https://navibeat.app/linux.html) &nbsp;&middot;&nbsp; [Report a bug](../../issues/new/choose)

</div>

---

## Beta software, please read

> **NaviBeat for Linux is in BETA.** It is built and tested on real hardware, but it is early, and **you may encounter bugs.** If something breaks, misbehaves, or looks wrong, that is genuinely useful to know: please [open an issue](../../issues/new/choose) so it can be fixed. This is exactly the stage where your reports shape the app.

The Apple builds (iPhone, iPad, Mac, Apple TV, Apple Watch) are shipping releases on the App Store. **The Linux build is the newest member of the family and the one still finding its feet**, so treat it as a beta and keep your expectations set to "promising, not polished."

---

## What NaviBeat is

NaviBeat is a **client**, not a server. It connects to a music server you already run and plays your own library from it. It does not host, stream, or provide any music of its own.

It works with:

- **Navidrome** (v0.50 or later)
- Any **OpenSubsonic** compatible server
- **Airsonic-Advanced**, **Gonic**, and classic **Subsonic** servers

The Linux app is a **real native desktop application** written in Kotlin with Compose Multiplatform. No Electron, no web view in a window, no browser tab pretending to be an app. It draws its own window, remembers where you put it, and integrates with your desktop's media keys.

<div align="center">

<img src="docs/img/home.png" alt="NaviBeat for Linux: Home with a Featured Album hero, Quick Play, Made for You and Most Played shelves" width="90%">

</div>

---

## Features

Everything the Linux build can do today.

### Your whole library

- **Home** with a Featured Album hero ("pick up where you left off"), Quick Play (Shuffle Mix, Random Album, Favorites, Random Artist), and Most Played
- **Made for You**: Time Machine and Year in Review, built from your own listening history on this machine
- **Smart shelves**: On This Day, Because You Listened, Replay, Discover Mix, plus Your Mixes and Your Last.fm once you connect an account
- **Artists**, **Albums**, **Songs**, **Genres**, **Playlists**, **Favorites**
- **Recently Added**, **Recently Played**, **Recently Released**
- **Internet Radio** stations configured on your server
- **Directories**: browse your library by its folder structure
- Full-text **Search** across artists, albums, songs and playlists

### Playing music

- **Now Playing** with album art, a quality badge (FLAC, MP3 bitrate, and more), star ratings, and full transport controls
- **Time-synced lyrics**, with an optional word-by-word karaoke mode when your server has the timing
- **Mini Player** in a compact window that stays on top of your other work
- **Continue where you left off**: resume a track partway through, or start it over
- **AutoMix** endless playback
- **10-band equalizer** (32 Hz to 16 kHz, plus or minus 12 dB per band), **ReplayGain**, and **crossfade**
- **Stream quality** picker: send the original file untouched, or ask the server to transcode to a lighter tier

### Offline and downloads

- **Download** tracks, albums and playlists for offline listening
- **Prefer Downloaded Music**: play the local copy when you have one, even while online
- **Offline Mode**: show and play only what you have downloaded
- Concurrent-download control and an LRU **cache size limit**

### NaviSyncRock: your library on a Rockbox player

- Send music to a connected **Rockbox iPod or player**, right from the app
- Your **server** does the transcoding; album art is re-encoded so old hardware renders it
- Playlists are written correctly, and plays made on the device sync back
- Set it up from **Settings > NaviSyncRock**, or just plug the player in and it appears in the sidebar
- **This is a paid add-on on the Mac. On Linux it is free.**

### Stats and services

- **Listening Stats** with a Recent Plays timeline
- **Server Health**: see how completely your server returns artist images, lyrics and album art
- Connect **Last.fm** and **ListenBrainz** for artist enrichment and personalized shelves

### Built for a homelab

- Custom **HTTP headers** for Cloudflare Access and Authelia
- **mTLS client certificates** for a server behind mutual TLS
- Works over **Tailscale** and behind your own reverse proxy, with no third-party relay in between
- **Multi-library** support

### Looks and desktop fit

- **Dark**, **light**, or **system** theme
- **Frosted Glass**: a translucent window, tinted for readability, that asks the compositor to blur behind it (KDE and picom oblige; GNOME shows the tint)
- Remembers its **window size and position**
- **Media-key and desktop integration** over MPRIS
- **Zero analytics, zero trackers**

<div align="center">

<img src="docs/img/now-playing-lyrics.png" alt="NaviBeat for Linux: Now Playing with a time-synced lyrics panel" width="49%"> <img src="docs/img/albums.png" alt="NaviBeat for Linux: the Albums grid" width="49%">

</div>

---

## Download

Grab the latest **AppImage** for your machine from the [latest release](../../releases/latest):

| Your machine | Download |
| --- | --- |
| **PC or laptop**, Intel or AMD, 64-bit | [`NaviBeat-linux-x86_64.AppImage`](../../releases/latest/download/NaviBeat-linux-x86_64.AppImage) |
| **ARM 64-bit**: Raspberry Pi (64-bit OS), Asahi Linux on Apple Silicon, ARM servers | [`NaviBeat-linux-aarch64.AppImage`](../../releases/latest/download/NaviBeat-linux-aarch64.AppImage) |

The AppImage is a single self-contained file. It carries its own Java runtime, so you do **not** need to install Java.

---

## Install

1. **Download** the AppImage for your machine from the [latest release](../../releases/latest) (x86_64 for most PCs, aarch64 for a Raspberry Pi or Asahi Linux).
2. **Make it executable:**
   ```bash
   chmod +x NaviBeat-linux-x86_64.AppImage
   ```
3. **Run it:**
   ```bash
   ./NaviBeat-linux-x86_64.AppImage
   ```

### Requirements

- **Linux x86_64 or ARM64 (aarch64)**, 64-bit.
- **VLC must be installed.** NaviBeat plays audio through your system's libVLC. Install it from your distribution:
  - Fedora: `sudo dnf install vlc`
  - Debian / Ubuntu: `sudo apt install vlc`
  - Arch: `sudo pacman -S vlc`
- **FUSE** to launch the AppImage by double-clicking. Most desktops have it; if not:
  - Debian / Ubuntu: `sudo apt install libfuse2`
  - or run without FUSE: `./NaviBeat-linux-x86_64.AppImage --appimage-extract-and-run`
- A **Navidrome or OpenSubsonic server** to connect to. NaviBeat is a client and does not come with any music.

On first launch you pair the app with your server: enter its address, username and password.

---

## Part of the NaviBeat ecosystem

This repository is **for the Linux build only**. NaviBeat is a whole family of native apps, and the Apple builds live on the App Store as a single **Universal Purchase** (buy once, use on every Apple device):

| Platform | Where to get it |
| --- | --- |
| **Mac** | [App Store](https://apps.apple.com/app/navibeat/id6763518834?platform=mac) &middot; [navibeat.app/macos](https://navibeat.app/macos.html) |
| **iPhone** | [App Store](https://apps.apple.com/app/navibeat/id6763518834?platform=iphone) &middot; [navibeat.app/iphone](https://navibeat.app/iphone.html) |
| **iPad** | [App Store](https://apps.apple.com/app/navibeat/id6763518834?platform=ipad) &middot; [navibeat.app/ipad](https://navibeat.app/ipad.html) |
| **Apple TV** | [App Store](https://apps.apple.com/app/navibeat/id6763518834?platform=appletv) &middot; [navibeat.app/appletv](https://navibeat.app/appletv.html) |
| **Apple Watch** | [App Store](https://apps.apple.com/app/navibeat/id6763518834) &middot; [navibeat.app/applewatch](https://navibeat.app/applewatch.html) |
| **Linux** | You are here. [navibeat.app/linux](https://navibeat.app/linux.html) |

The Linux build is **free**. The Apple builds are a one-time $5.99 Universal Purchase.

Website: **[navibeat.app](https://navibeat.app/)**

---

## Feedback and bug reports

The Linux build is beta, and your reports are how it gets better.

- **Found a bug?** [Open a bug report](../../issues/new/choose).
- **Have an idea, or a question?** Start a [Discussion](../../discussions) or open a [feature request](../../issues/new/choose).

When you report a bug, the more you can tell me about your distribution, desktop environment and server, the faster it gets fixed. The issue templates ask for exactly what helps.

---

## Support the developer

NaviBeat for Linux is free, with no ads, no tracking and no subscription. If it earns a place in your setup, a coffee genuinely helps and means a lot.

<div align="center">

[<img src="https://img.shields.io/badge/Buy%20Me%20a%20Coffee-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=black" alt="Buy Me a Coffee">](https://buymeacoffee.com/nenadjokic)
&nbsp;
[<img src="https://img.shields.io/badge/PayPal-0070BA?style=for-the-badge&logo=paypal&logoColor=white" alt="PayPal">](https://paypal.me/nenadjokicRS)

</div>

---

## Privacy

NaviBeat talks to your server and to nobody else. There are no analytics and no trackers in the app. Full policy at [navibeat.app/privacy](https://navibeat.app/privacy.html).

## License

NaviBeat for Linux is **free to use, but it is not open source.** It is proprietary software, and this repository holds only the release binaries and documentation, never the source. You may download and use it at no cost; you may not copy, redistribute, modify, reverse engineer, or reuse it. See [LICENSE](LICENSE) for the full terms.

## Updates

Every update ships here as a new release with the binary attached and a **What's New** note. Watch this repository, or check [Releases](../../releases), to stay current.

---

## How I build NaviBeat

NaviBeat is my hobby project, and I genuinely love it. I build the app I want to use myself first, and then I share it with the world.

Keeping this many native builds moving on my own is hard: macOS, Apple TV, iPhone with its Watch app, and now Linux. So I lean on agentic coding heavily. I actively use Claude Code to help me navigate the code, chase bugs, and work through change requests. That is what lets one person keep all of these apps in sync.

By day I am a Business Analyst, working mostly on direct-to-consumer products at a large FMCG company. I know a few programming languages reasonably well, but my real strength is the logic and the requirements: how a thing should behave, and how to express that across different syntaxes. So I do not just vibe-code. Every change becomes a proper, DevOps-style backlog task: I groom it, then push it through development, UAT, public beta, and finally production. There is real Q&A on my side.

Still, people are only people, and I can miss things. That is why I rely so much on beta testers filing bugs and change requests, and it is why your reports genuinely matter. If anything in the app ever feels like too much AI, or just feels off, please reach out. I am always happy to fix it and run another round of CRs to make NaviBeat better.

The code itself stays private and proprietary. The agents only make the building faster.

<div align="center">

Made with care in Belgrade by Nenad Jokic. &nbsp;&middot;&nbsp; NaviBeat is not affiliated with the Navidrome or Subsonic projects.

</div>
