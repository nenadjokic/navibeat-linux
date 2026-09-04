# What's New

Every release attaches a fresh AppImage. Newest first. Each version's full note is on its
[release page](../../releases).

## 0.10.0 (beta)

- The artwork shrinks a little while paused and springs back on play. Lyrics get a text size and an active line colour in Settings, a soft shadow on the line being sung, a pause line between verses that fills in until the next verse, and line changes that glide. The blurred backdrop is painted once per song, so it stays still while the lyrics scroll.
- Terminal client: Now Playing on the big screen is rebuilt with the sleeve on top and everything under it, and three new keys: `m` for AutoMix, `z` for the sleep timer, `*` then a digit to rate.
- Settings: "Hide NaviBeat Mixes in Playlists", "Show Upcoming Concerts on Artist Pages", custom HTTP headers editable after pairing (checked against the server before they are saved), and Customise Home moves exactly the row you moved, Favorited included.
- "Continue here" pauses the device you left and starts where that device really is. "Pick up where you left off" offers an album only when the queue was that album. After a resume the clock and the scrubber agree with what you hear.
- Back on the keyboard: Alt+Left or Ctrl+[ pops the page like the toolbar chevron, the mouse's back button does the same, and the command palette lists Back.
- MPRIS `SetPosition` moves the song, so `playerctl position 90` and desktop widgets that seek to an absolute time work (GitHub #16).
- Rockbox sync keeps several songs in flight and starts the next one the moment one lands.
- Android: swipe the artwork on Now Playing to change songs, with a cover-flow tilt; the same lyrics settings, pause line and paused artwork; Top Songs shows the best five. Android TV gets the lyrics settings, the pause line, the paused artwork, and genre chips on the album page.

## 0.9.99 (beta)

- A downloaded song remembers the quality it was fetched at; the player badge shows that quality and Get Info gains two lines under Bitrate, the quality asked for and the bitrate measured from the file.
- A saved speaker that does not answer is listed greyed with "Not found. It may be off, or something else has its address." Right-click it to rename or forget it.
- The first-run wizard's Scrobbling step carries ListenBrainz beside Last.fm.
- OFFLINE replaces the download word on the quality badge while the server is away, and the Last.fm listener count reads "L.FM".
- A transcoded stream whose decoder guesses a wildly wrong length uses the library's own duration.
- The NaviFin card in "More from Nenad Jokic" opens the App Store.
- Android: lyrics keep time with the singer, a song that will not decode skips to the next one, the listener count names its source, Get Info gets the two download lines, and a downloads database that will not open is moved aside and kept.

## 0.9.98 (beta)

- Some albums have a track you never want to hear. Right-click any song and pick "Skip this song when the album plays". It stays in the album, greyed with a mark, and it never enters the queue when you press Play. Play it directly and it still plays.
- Cast to a UPnP speaker once and it is written down, so it comes back next time even if it answers no search. Right-click a saved speaker to rename it or forget it, and the name you give it is the name you see.
- Album and track credits use one separator everywhere.
- A play or pause press can no longer leave the player claiming it is playing with an empty queue. It rebuilds the queue instead.
- Installing an older build over a newer one no longer drops the record of which downloaded files belong to which track.

## 0.9.97 (beta)

- Playlist covers now get the same Shuffle and Play buttons on hover that album covers have, and the downloaded mark moves clear of them.
- Rockbox sync shows one progress bar for the whole run, a checklist of the steps, and the songs being copied listed by name.
- On KDE you can drag the window freely onto a second monitor.
- The "can't reach your server" banner is far less trigger-happy: a single dropped request no longer turns the app red.
- Terminal player: Now Playing splits evenly with Up Next and lyrics.
- Casting on Android: "Stop Cast" keeps your place instead of jumping to the first song, and the phone stays paused rather than starting playback on its own.
- Android: Back returns to where you came from, Home or Search, instead of always Library, and songs in a playlist have a long-press menu with Show Album.
- Android Auto: when your car turns on, NaviBeat comes back to your saved queue, paused where you left off.
- Android TV: a proper widescreen launcher banner, a sign-in screen that scrolls so the Connect button and status stay visible, the on-screen keyboard opens when you press a field, and an option to fit non-square cover art instead of cropping it.

## 0.9.96 (beta)

- Downloads is a tree in the terminal client: artist, album, song, and every branch says what is
  happening under it. Press `t` on Songs and your whole library folds into the same shape, with how
  many songs and how long sit on each branch, and how much of it is already on this computer.
- Troubleshooting, new under Settings, About. Switches for playback, downloads, artwork, scrobbling,
  casting and a plugged-in Rockbox player, everything off until you turn one on, and a Prepare log
  button that writes a file into your Downloads folder. Your server address, your username and
  anything that looks like a credential are stripped from every line before it is written.
- A cover shown whole sits on a blurred copy of the sleeve instead of a flat bar.
- The Rockbox panel names the tracks it is copying rather than counting them, and each one carries
  its own progress.
- Lyrics animation speed: Smooth, Fast or Instant.
- Record labels are a place you can browse.
- Search finds what you type when an artist and a title go in together.
- Home shelves can hide entries that are not in your library.
- A TUI button beside minimise and maximise hands the window over to the terminal client.

## 0.9.94 (beta)

- Now Playing is rebuilt. It opens over the whole window and splits it down the middle: the player
  on the left, your lyrics or your queue on the right, and a capsule in the corner to swap them.
  Closing it puts you back exactly where you were, on the same page and at the same scroll position.
- The artwork grows into its own half on a wide display instead of stopping at a fixed size, and it
  sits centred there rather than pinned to the edge.
- Lyrics and Up Next open as a floating card over the content on every other screen, with their own
  close button, instead of a column pinned to the side.
- The playing bar floats. Album covers slide underneath it instead of stopping at a line across the
  window, and the last row of every list stays reachable.
- Track position, off by default: a line like "Track 3 of 11" under the album on Now Playing.
  When what is playing is not one whole album it counts your queue and says so instead.
- Explicit songs are marked with an E after the title, on song rows, album headers and Now Playing,
  taken from your server's own tag.
- Search has a "Found in lyrics" section for the songs you have downloaded, and each result shows
  the line that matched.
- Lyrics grow with the panel. A wider window gets bigger words rather than more empty space.
- Long artist biographies open properly in every language, including Japanese, Chinese and Korean.
- The check that decides between your home address and your public one no longer waits behind the
  app's own traffic, and Settings, Server addresses has a Check again button beside it.

## 0.9.93 (beta)

- Play at the end of a playlist starts it again from the first track, and so does Play after
  skipping past the last song.
- The library keeps your place. Open an album, come back, and the list is where you left it, in
  every tab that has one.
- A tunnel no longer counts as being at home. On someone else's Wi-Fi with a VPN up, the app was
  treating the home address answering as proof you were on your own network and streaming at the
  home quality tier; it now checks whether this machine shares the server's subnet.
- With no network at all, browsing goes straight to your downloads instead of waiting for a request
  to time out first.
- New in Settings: Show disc number. Off shows only a disc's own subtitle, and a disc without one
  draws no header at all.
- The artwork swipe tells a skip from a dismiss by the whole gesture rather than its first
  millimetre.
- The Playlists toolbar plus offers both a plain and a smart playlist, and the Smart Playlists
  section stays out of the way until you have one.

## 0.9.92 (beta)

**Get Info on any track.** Right click a song and the panel opens with everything your server
said about that file: the credited artists, the original release date, the format, the sample
rate, the bit depth and the channels, the size and the path, MusicBrainz and ISRC, the
ReplayGain values, and the Comment tag. Every value is selectable, so an id or a path can be
copied straight out of it.

**The NaviBeat Mixes covers are redrawn.** Each mix carries its own symbol as a watermark under
the NaviBeat seal, and the gradients run the way the artwork was designed to. A mix whose name
starts with an emoji drops it on the tile and keeps it in the caption underneath, so the
artwork stays clean and the playlist keeps its name.

**Your Last.fm and Your ListenBrainz fill in on a cold launch.** Top artists arrive with their
pictures and open the artist page on a click. Top tracks find their album art and play.

**In the terminal client, Up Next is walkable from the big Now Playing screen.** The arrows or
`j` and `k` move a cursor through it, enter plays what is under the cursor, `x` takes a song
out, and the list scrolls so the fifth song is reachable. The transport strip gained a volume
bar and marks for shuffle and repeat beside the clock.

## 0.9.91 (beta)

**Drag anything onto your Rockbox player.** An album, an artist, a whole playlist or a
selection of songs, from any list in the library, straight onto the player in the sidebar. A
card follows the cursor with the cover and the name of what you are carrying, and the player
row lights up when it is ready to take it.

**The send panel is a window of its own.** It floats above the app, so a transfer started from
a drag or a menu is visible wherever you are: the track in flight with its own progress, the
whole job, what is queued behind it, and separate Skip Current and Cancel All.

**Send to RockBox from the playlist page**, and every row on the Downloads screen can be
dragged to the player too.

**Shuffle part-way through a playlist now shuffles what is left.** What you have already heard
stays in Earlier in Queue, in the order you heard it.

**Play on an artist starts their newest release** and queues the whole catalogue behind it,
newest to oldest. Top Songs, Shuffle and Radio are the other three buttons and each still does
its own job.

## 0.9.90 (beta)

- **Changing the send format now replaces the files on your player.** An MP3 library sent as MP3
  keeps the same filenames, so switching it to Original (or to any other format) used to hit the
  "skip files that are already there" rule and leave the old encodes in place. A format change
  replaces, whatever the duplicate setting says.
- **A track that fails to transfer is no longer recorded as delivered.** The player's own record is
  written from what actually landed, so anything that failed is picked up by the next sync instead
  of being remembered as done.
- **Click the time on the right of the scrubber** to switch it between time remaining and the total
  length of the track. Elapsed stays on the left, the choice is remembered, and it works on Now
  Playing, in the player bar, in the mini player and in the terminal client.
- The **Libraries** picker in Settings opens over the whole window.

## 0.9.89 (beta)

- **NaviSyncRock can send the original file.** A new **Original (no transcode)** option in
  Settings > NaviSyncRock copies the file your server already has, untouched: same format, same
  bitrate, nothing re-encoded. The name on the device follows the real file, so a FLAC arrives as
  `.flac`. Rockbox plays FLAC, ALAC and WAV, and those files are several times larger than an MP3,
  so keep an eye on the space. DSD is the one exception: no Rockbox player decodes it, so those
  tracks are sent as FLAC.
- **The send settings are in Settings now**, as one Send Format card: format, bitrate, album art
  size and what to do about a file that is already there. The connected player's manufacturer,
  model, screen and serial show there too.
- **Lyrics your own server does not have.** A new switch in Settings > Lyrics, off until you turn it
  on, asks lrclib.net for songs your server has no lyrics for. Your server is always asked first and
  its lyrics plugin gets a moment to answer; only when neither has anything does NaviBeat ask, and
  it sends just the song title, artist, album and length.
- **The quality badge has a switch.** Settings > Now Playing turns the codec and bitrate chip off on
  Now Playing, in the player bar, in the mini player and in the terminal client.
- **Speakers has its own section** under Settings > Devices, opening the UPnP and DLNA picker.

## 0.9.88 (beta)

- **Crossfade now runs on streamed songs**, not only on downloaded ones. NaviBeat quietly fetches the
  playing song's file in the background, and once it has landed the end of that song can overlap the
  start of the next. If it has not landed by the time the fade would start, the song ends the normal
  way. Nothing is ever fetched a second time from your server for the fade: a server transcoding on
  the fly ignores a request for the end of a file and sends the beginning instead, so a tail pulled
  from the server would fade out the opening of the song you are leaving. Off by default, in Settings
  under Playback and Audio, one to twelve seconds.
- **The same album no longer appears more than once.** With more than one music folder selected, an
  album, artist or song living in two of them was drawn once per folder, so Recently Added could show
  the same record three times. Fixed on album lists, artist lists and genre browsing, and your
  server's own ordering is kept.

## 0.9.87 (beta)

- **Install it with `pacman`.** A signed pacman repository now sits beside apt and dnf, for Arch
  Linux and Arch Linux ARM. It uses the `libvlc` already in Arch's own repositories, which is how a
  package on Arch is expected to behave; the Debian and Fedora packages keep their own copy.
- **The terminal client opens with a proper welcome.** Run `--tui` on a machine that has never seen
  NaviBeat and you get the mark drawn in terminal cells, the server address, username and password on
  one card, custom HTTP headers and a client certificate a keystroke away, and a live meter while it
  reaches your server. A six page setup wizard follows, so the terminal asks everything the window
  asks on a first run.
- **Karaoke lyrics in the terminal**, filling each line in as it is sung, word by word where your
  server has the timings. `K` cycles the style, and it shares the setting with the window.
- **Album pages stop truncating.** A movement title is no longer cut where every movement looks the
  same, work headers wrap, and a disc header keeps its number when the disc also has a name.
- **Now Playing, Cover first or Text first.** A setting that hands the artwork's height to the title
  and the performers, for libraries where every sleeve is the same picture.
- **Favourites as a way to browse**, across songs, albums and artists, and it survives a restart.
- **The Downloads filter lists playlists a mirror completed**, not only the ones downloaded as
  playlists.
- **Home refresh reaches every shelf**, so a playlist deleted on the server disappears when you ask.
- **A stream that dies mid track holds the song on every path it can fail on**, including a
  connection dropped by a tunnel or a proxy, and the log now says why a track was judged finished.
- **Coming home switches the next track to your lossless copy immediately** rather than a few tracks
  later, and an AAC download from Navidrome is saved under a name that opens.
- Clicking the launcher icon of an already running NaviBeat raises the window.

## 0.9.86 (beta)

- **Settings is seven groups instead of one long scroll**: Server & Library, Playback & Audio,
  Appearance & Language, Scrobbling & Stats, Devices, Downloads & Storage, About.
- **Settings has a search box** that knows the words people actually type: "bit perfect" finds
  Direct Playback, "gapless" finds the switch, "eq" finds the equalizer. Each result names the
  section it lives under.
- **Made for You is one shelf with a badge for every source feeding it**, Last.fm, ListenBrainz and
  AudioMuse on a server that runs the plugin. The ListenBrainz weekly mixes moved into that shelf.
- **A transcoded song whose download fails now streams** instead of trying the same download again.
- **Continue here plays the song on the card**, even when the queue saved on your server belongs to
  a different session.
- **Every label on the accent colour is derived from the colour you picked**, so no accent makes a
  button unreadable.
- **Your library selection reaches the whole-genre shuffle, smart playlists** and the shelves that
  resolve a song by name.
- **Speakers can be added by typing an address** when the search does not find them, including the
  description path Denon and Marantz receivers use.

## 0.9.85 (beta)

- **Covers appear the moment they arrive.** Every grid, shelf and sleeve puts artwork on screen as
  soon as it is ready, with the pointer anywhere you like.
- **A song that stops short is finished properly**: a stream that ends earlier than the track really
  is gets picked back up and played out.

## 0.9.84 (beta)

- **Play it on the speakers and televisions you already own.** The Play on menu lists the UPnP and
  DLNA renderers on your network, and NaviBeat serves the audio from this machine, so anything in
  your library reaches the device whether or not it has heard of your music server.
- `navibeat --cast-scan` prints what this machine can see, from the terminal.

## 0.9.83 (beta)

- **Downloaded albums read in disc and track order** on the Downloads screen, the same order the
  album has on its own page.
- **Your downloaded playlists are on the Downloads screen**, grouped under Playlists with the songs
  of them that are on this machine.
- **A stutter between you and your server no longer ends the song**: a connection that drops for a
  moment is treated as the interruption it is and the music carries on.
- **AutoMix gets the last word** at the end of the queue and keeps the music going.
- **Frosted glass can always be switched back off**: a window closed by force with the setting on
  opens plainly the next time, so Settings is never behind the glass.

## 0.9.82 (beta)

- **A service that cannot be reached says so**, in a sentence about the network rather than about
  your account, with a way to try again.
- **The address you see in Settings is the address the page behind it lists**: the Saved Servers row
  and the Saved Servers page read from one place.
- **Three window buttons**: minimise, maximise and close, with full screen on F11.
- **Casting says something when a device does not answer**, and the music comes back to this machine
  at the second it left.

## 0.9.81 (beta)

- **Searching a list searches your whole library**, so the match comes back from everything on your
  server rather than from the rows already loaded on screen.
- **Sorting stays where you put it**, and it is still the order you chose the next time you open
  NaviBeat.
- **A new server address is checked before it is saved**, so the address you end up with is one
  that answers.
- **The cache limit is enforced.** The copies kept automatically while you stream are the ones that
  make room, and the downloads you asked for stay where they are.
- **The equalizer's band controls reach playback and stay set**: presets, the ten bands and the
  parametric band frequencies.
- **Every credited artist is its own link**, wherever a song is listed.
- **A song opened through a genre carries its full controls**: the heart, the whole right click
  menu, and Shuffle on the page you found it on.

## 0.9.80 (beta)

- **Browsing your downloads narrows the whole library.** With the downloaded only filter on, every
  grid and every list shows what is on this machine, and scrolling further keeps you inside it.
- **An album cover opens full size**, uncropped, the whole square as your server holds it.
- **Every credited artist is its own link**, on the album page, on the tile in the grid and on the
  shelf at home.
- **Saving the queue makes a new playlist**: Save from Up Next opens the new playlist form and
  creates it when you say Create.
- **Time Machine takes a date range**, a start date and an end date, filled in with the last
  thirty days.
- **Search starts from an empty field** when you reach for it again.

## 0.9.79 (beta)

- **Every screen laid against its Mac twin.** A list, a grid, a row and a menu are the same size
  and carry the same words on either machine, down to the sentence under a section.
- **The same menu wherever you right click**, on a song, an album, an artist, a playlist and a row
  in the sidebar, with rating as a submenu and a two step Remove Download on a song already here.
- **Composers finds every composer your server credits**, however your files are tagged.
- **Album, artist and playlist pages carry what the Mac carries**: similar tracks and similar
  albums, your server's own biography and counts, and star ratings in a column of their own.
- **Settings gained the screens it was missing**: What's New & Tips, the open source notices with
  each licence in full, Library statistics read from your server, a corrections list you can add
  to, jump buttons, and Shuffle Exclusions on a screen of its own.
- **Every heading in Downloads opens the collection it names**, and the download queue has a
  screen of its own.

## 0.9.78 (beta)

- **Browsing tells you the truth about what it is showing.** A playlist, an album and an artist
  page open with everything they really hold, and the numbers beside them are the server's own.
- **Albums play in their own order**, disc by disc and track by track, including music you
  downloaded before track numbers were kept.
- **Every cover keeps its own tile** as a grid scrolls.

## 0.9.77 (beta)

- **A command palette on Ctrl+K**: one field that reaches every screen and every playback action
  without leaving the keyboard.
- **A setup wizard**, six pages after your first pairing, so the app arrives configured.
- **Smart playlists on the desktop**: build a playlist out of rules and it keeps itself current.
- **Year in Review**, five slides with a card you can share.
- **A ten band equalizer**, presets and a preamp, applied live.
- **Servers behind Cloudflare Access or Authelia connect**: client certificates and custom HTTP
  headers are enterable at pairing.

## 0.9.76 (beta)

- **A playlist downloads from its own page.** The button reads how much of it is already here:
  Download 7/12 while it fills, Downloaded when it is complete, and a second press gives the
  space back.
- **Playlist rows carry the full trailing cluster**: stars, heart, download mark and running time.
- **A starred song already on this device looks like it.**

## 0.9.75 (beta)

- **Similar Albums sits at the foot of an album**, so the record you are looking at suggests the
  next one.
- **Every track menu offers the same verbs wherever you open it**, grouped so the one you want is
  where your eye already went.
- **Favorites got the row the rest of the app uses**: cover art, stars, heart, download mark and
  running time, with a right click that offers everything.
- **Genres can be ordered by size or by name.**

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
  request is fetched again.
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
