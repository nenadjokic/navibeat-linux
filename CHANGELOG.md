# What's New

Every release attaches a fresh AppImage. Newest first. Each version's full note is on its
[release page](../../releases).

## 0.9.54 (beta)

**NaviBeat runs without a desktop.**

- **A full terminal client**: `./NaviBeat-linux-x86_64.AppImage --tui`. On a machine with no
  display it starts that way by itself, so a Raspberry Pi or a headless server plays your library
  over SSH.
- Ten screens on the number row, album, artist, playlist and genre screens behind them, server
  search, list filter, queueing, favourites, downloads and pairing on first run.
- Keys a terminal listener already knows, with `?` for the whole map, and the arrows working
  alongside them.
- NaviBeat's colour on the progress bar where the terminal has it, stepping down to 256 colours,
  16 colours and finally ASCII. `--colors=` and `NO_COLOR` are honoured, and everything else takes
  your own palette.
- `playerctl` and the media keys see the terminal client exactly as they see the window.
- **One player per account**: starting NaviBeat while it is already running brings the open window
  to the front instead of starting a second copy.

## 0.9.32 (beta)

The first public beta of NaviBeat for Linux, on both x86_64 and ARM64.

- Ships for **x86_64** (Intel/AMD) and **ARM64 (aarch64)**: Raspberry Pi 64-bit, Asahi Linux on Apple Silicon, ARM servers
- Native desktop client for Navidrome, OpenSubsonic, Airsonic-Advanced, Gonic and Subsonic
- Full library: Home shelves, Artists, Albums, Songs, Genres, Playlists, Radio, Directories, Search
- Now Playing with time-synced lyrics, a Mini Player, AutoMix, a 10-band equalizer, ReplayGain and crossfade
- Downloads and offline playback, with Prefer Downloaded Music and an Offline Mode
- NaviSyncRock: sync your library to a Rockbox iPod or player, free on Linux
- Listening Stats, Server Health, and Last.fm and ListenBrainz linking
- Homelab-friendly: custom HTTP headers, mTLS client certificates, Tailscale, multi-library
- Frosted Glass window, dark, light and system themes, and MPRIS media-key integration
- Ships as a single self-contained AppImage with its own Java runtime
