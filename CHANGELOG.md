# What's New

Every release attaches a fresh AppImage. Newest first. Each version's full note is on its
[release page](../../releases).

## 0.9.74 (beta)

- **Your whole library can stay downloaded.** Switch on Offline Library in Settings and NaviBeat
  keeps every album on this machine by itself, so the music is there whether the server is or not.
- **A playlist you have downloaded opens with no connection**, with its songs in the order you
  saved them, and a downloaded playlist carries a mark on its cover so you can see at a glance
  what is already on disk.
- **Lyrics also come from a lyrics plugin on your server.** If your server has one, its words
  reach the Now Playing page and the terminal client along with everything else.
- **The Last.fm listener count travels with the song**, on the playing bar, on the Now Playing
  page and in the mini player.
- **The artist and the album under the playing title open their pages.** Click either name and
  you are there, with the music playing.
- **Every shelf on Home lifts under the pointer** and offers Play and Shuffle where your hand
  already is.
- **Cover art keeps trying until it arrives.** A picture that does not come through on the first
  request is fetched again rather than left as it was.
- **The library sorts the way the Mac does**, with numbers read as numbers rather than as text.

## 0.9.73 (beta)

- **Handing playback over is instant, wherever you are in the track.** Press Continue here on your
  phone, tablet or another desktop and this machine steps aside within a single poll. Taking a song
  over three minutes in now works exactly like taking it over three seconds in.
- **The sidebar reaches the bottom of the window**, and the playing bar sits centred over the column
  it belongs to rather than spanning the frame.
- **A server that stops answering says which request stopped.** The log names the failing call and
  the reason, so a connection problem can be traced from one run.

## 0.9.72 (beta)

- **Choose your audio output and device.** Settings > Playback names the sound system NaviBeat plays
  through and the device inside it. Both lists are read from your own VLC, so you see exactly the
  modules it has, with its own descriptions. ALSA straight to a DAC's hardware entry addresses the
  card rather than the sound server.
- **Saved servers.** Save the server you are on, save the others as you pair with them, and each is a
  two-click switch carrying the address, the account, the password, any proxy headers and a client
  certificate. With two or more saved, the sidebar names the active one with the others one click
  away. The switch pings the target before it changes anything, so a server that is asleep costs an
  error message and not the pairing you had.
- **DSD plays.** A `.dsf` or `.dff` used to run the progress bar over silence: libVLC 3 carries no DSD
  codec mapping, so the file opens, the stream arrives as an unknown codec and nothing is rendered.
  NaviBeat now asks the server for FLAC instead of the untouched file, losslessly. A deliberate lossy
  tier on a metered link still wins.
- **A ListenBrainz instance of your own.** Put its address beside the token and NaviBeat talks to that
  one instead of the public service. Similar-artist lookups against the public Labs host stop, so
  nothing about your listening goes to a service you left.
- **A genre tree built from your own tags.** Off by default, separator configurable. `Rock - Metal -
  Alternative` becomes a browsable tree and tags without the separator are left alone.
- **Answer your desktop's search box**, optional and off by default. Your artists and albums appear in
  the GNOME overview. Nothing is copied into a system index: the shell asks NaviBeat while it runs.
- **Mixes as buttons** when the NaviBeat Mixes plugin asks for that style, with the server's own icon
  and colour per mix.
- **Downloads waiting their turn are visible** under "Up next" instead of appearing to have been
  dropped.

## 0.9.71 through 0.9.60 (beta)

Casting to UPnP speakers, the Rockbox sync sweep and its zero-byte repair, the terminal client's Now
Playing screen and its lyrics that no longer get cut, the artist and album enrichment sources, the
first three GitHub issues from Fedora and Niri, playlist mirroring, smart playlist screens, and the
Windows parity round. Each one's full note is on its own
[release page](../../releases).

## 0.9.59 (beta)

- **Now Playing, full screen, in the terminal.** The cover takes as much of the frame as it can hold,
  with the track, the artist, the album, the year and the format beside it, then what is coming next
  and the time-synced words. First thing on Home.
- **`H` and `L` move the divider** between the library and the side column, two cells at a time.
- **Cover art on more terminals.** Terminals that do not announce a colour depth now get the full
  palette, so covers arrive as pictures across a much wider range of SSH clients and emulators.
- Resizing the window repaints the whole frame, so the screen is as clean after a drag as before it.

## 0.9.58 (beta)

- **Guess the Year deals from your whole library**: your favourites and your Home shelves as well as
  your songs, and it has a round ready the moment you open it.

## 0.9.57 (beta)

- **A log with the time on it** above the transport: what you queued, favourited or downloaded, kept
  on screen instead of a toast you missed. It appears only while something is recent, and **Activity**
  on Home has the whole session.

## 0.9.56 (beta)

**The terminal client stops being a list.**

- Every section in its own frame, in NaviBeat's amber, with the focused one drawn in the app's own
  red to orange gradient.
- The library, Up Next and time-synced lyrics on screen at once. `Tab` moves between them; `enter`
  in the queue jumps to a track, `enter` in the lyrics seeks to that line; `w` turns the side panes
  on or off per screen.
- **Cover art in the terminal**, one cell carrying two pixels in full colour, on album and artist
  pages and beside the transport.
- **Listening**, a heatmap of your own play log, seven days by twenty four hours, with your top
  artists, albums and songs.
- **Guess the Year**, a track from your library with its name hidden and four years to pick from.
- A line along the bottom that always shows the keys that work where you are.

## 0.9.55 (beta)

- Cover art in search results, and square tiles instead of stretched ones.
- Connect Last.fm opens your browser on desktops where it did not before, and the authorize address
  is on screen with a Copy button while linking.
- The same filter field on Albums, Artists, Songs, Playlists and Downloads.

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
