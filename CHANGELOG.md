# Changelog

All notable changes to FabStream. Each release on GitHub shows the section of its version.
Format: Added / Improved / Fixed / Known issues.

## 4.9.0 – 2026-10-10

### Added
- **Edit every track on its own in the Auto-Cutter:** cut a single track with the new **cut tool** (*C*, or the *Cut tool* button – Shift + click cuts every track) or at the playhead (*K*), then mute just that part of your mic, Discord or game sound (*M*, or right-click it) and set each track's volume (0–200 %). Cut a part of the picture out of the clips (*X*) – it's removed from every track so picture and sound stay in sync. Clips with edits show a ✂ and their length after cutting; the preview plays what the clip will sound like and skips the parts you cut out. Edits are kept per recording while FabStream runs. Limit: clips with a part cut out are re-encoded, so cutting them takes longer than before.
- **Right-click everywhere in the Auto-Cutter:** tracks (split, mute or cut out a part, remove a cut, volume, mute / solo, reset), track names, clips on the timeline and in the list (play, loop, start / end at the playhead, formats, remove), the previews and the ruler (add a highlight, zoom, undo / redo).
- **Editor settings and undo:** right-click the timeline → *Settings*: follow the playhead while playing, snap to cuts, clips and the playhead, show the signs under the timeline (remembered). **Ctrl + Z / Ctrl + Y** undo and redo highlight changes and track edits.

### Improved
- **Upgrade or downgrade anytime – one license per account:** *Account → Licenses → Change plan* opens the plan switch (Premium, Ultra, Max, monthly or yearly). Upgrades start right away and you only pay the difference for the rest of your period; downgrades and switching from yearly to monthly take effect when the paid period ends. If you already have a subscription, the buy buttons on the website and in the app take you to this plan switch instead of starting a second subscription.
- **Buying now goes through your FabStream account:** sign in (or create your free account) first, then pay – your license is linked to your account right away and shows up on every PC you sign in to.
- **A calmer, clearer checkout page:** your order on top – plan, price per month or year, what's included, "incl. VAT" and the total – and the payment form in full width below, so on a computer it shows the price breakdown and the payment fields side by side instead of one long column. Switch between monthly and yearly or another plan right there (the yearly saving is shown), the header only keeps the logo and the language, and on phones the payment form comes right after the order.

## 4.8.1 – 2026-10-10

### Improved
- **Pay right on fabstream.fabcomstudios.com:** the payment form now opens on our own checkout page instead of a separate Stripe page – in FabStream's dark look with the gold button, next to an always-visible order summary: your plan, the price in the currency you pay in, VAT and the total due today (Stripe folds its own breakdown away on smaller screens – ours stays open).
- **Save your card for next time:** the payment form offers to remember your card, and businesses can add their VAT ID. Cards, Apple Pay, Google Pay and more work as before.

### Improved (app)
- **Smoother stream while you arrange your scene:** moving or resizing a source in the preview no longer rebuilds the scene list, the bot cards and the audio list on every mouse move, and the whole drag is saved as one undo step at the end. In our measurement with a large project (20 scenes, 300 items, a 2000-track playlist) the work per mouse move dropped from about 8 ms to under 2 ms, and doubled frames while dragging fell from 40 % to 11 %.
- **Animated browser sources don't take the studio's time any more:** the pages of browser sources (alert boxes, overlays) are converted to pixels in a separate background thread and the conversion is about twice as fast. A full-screen animated 1080p page used to take half of the time FabStream needs to draw your stream, which showed up as stutter – now it takes about 1 %.
- **Lighter autosave:** saving the project no longer reads the previous file again just to back it up.

### Fixed
- **Stream widgets with a video filter in both formats:** a widget (goal bar, alert box, chat …) with a filter was drawn into the 9:16 picture from its 16:9 version – squeezed and the wrong size. Each format now gets its own picture again.
- **No "What's new" on a fresh installation:** new users saw the release notes of every version right after skipping the setup assistant; now they only get the short app tour.

## 4.8.0 – 2026-10-10

### Added
- **Invite & earn now pays out directly:** your 20 % commission is paid by FabStream once a month – to your PayPal account or by bank transfer (IBAN). Enter where it should go on the website under *Account → Invite & earn*; the app shows it in *Invite & earn → Payout* together with your next payout, what is still in the 30-day refund period and what was already paid. No affiliate program to join any more.

### Improved
- **New checkout with Stripe:** subscriptions are now bought through Stripe – cards, Apple Pay, Google Pay and more. Existing subscriptions keep running as before.
- The commission is 20 % of what a subscription pays without VAT; amounts under 20 are carried over to the next month.
- The terms now contain the full EU withdrawal notice and a model withdrawal form.

## 4.7.0 – 2026-10-10

### Added
- **Connect your Riot account in one click:** *Settings → Games → VALORANT → Connect Riot account* now takes the account that is signed in to the Riot Client on your PC – no browser, no password, no waiting for Riot. The card shows your Riot ID and warns when another account is signed in to the Riot Client (*Update* switches to it). Kills, aces and clutches after each match still need Riot's approval of FabStream for its match data; won rounds and match results work live.
- **"Open" next to "Copy":** every link you can copy now also opens with one click – the phone remote address (shows FabStream Remote in your browser), the remote address for Stream Deck & co., and your invite link.

### Improved
- **Nicer buttons in the settings pages:** gold main buttons, value fields with attached *Show · Copy · Open* buttons, and a proper "locked" tile for the phone sign-in QR code (it was squashed in the settings window).

### Fixed
- **Game and window capture back at your frame rate:** 4.6.1 captured games at twice the frame rate. On a gaming PC with an uncapped game that made it worse (about one doubled frame in four instead of one in seven), so capture runs at your stream's frame rate again.
- **See when the game itself stutters:** while you are live or recording, the status bar shows *capture xx* and turns amber when a captured game, window or screen delivers clearly fewer new pictures than your stream needs. The tooltip says what helps: cap the game's frame rate, play in borderless/windowed fullscreen, turn on "Hardware-accelerated GPU scheduling", or capture the display instead of the window.
- The log no longer repeats "YouTube viewer count failed" every minute when your YouTube account cannot go live yet: it is written once, and FabStream asks YouTube again every 10 minutes.

## 4.6.1 – 2026-10-10

### Fixed
- **Fewer doubled frames in game and screen capture:** FabStream now captures games and screens at twice your output frame rate (120 for a 60 fps stream). Before, the capture and the output ran on two separate 60 Hz clocks, and about one frame in ten was shown twice in fast motion – visible as micro-stutter in streams and recordings. Older recordings keep the problem.

## 4.6.0 – 2026-10-10

### Improved
- **Much sharper recordings and replay clips:** recordings no longer share the stream's bitrate. With an NVIDIA, AMD or Intel encoder FabStream now encodes the same picture a second time in high quality just for recordings and the replay buffer (about 19 Mbit/s at 1080p60 instead of your 5–6 Mbit/s stream) – your stream keeps its bitrate. Choose *High* (default), *Maximum* or *Same as the stream* in *Settings → Recording → Quality*.
- **Sharper stream at the same bitrate on NVIDIA:** adaptive quantization and look-ahead are switched on where the graphics card supports them – more detail in dark and fast game scenes, fewer blocks.
- **Smoother motion:** *Settings → Video* warns when 50 or 25 fps are set – games and screens run at 60/120/144 Hz, so 50 fps skips every sixth frame or so and motion stutters (choose 60). The status bar turns amber with a ⚠ when the picture is not drawn evenly while you are live or recording, and says what helps (cap the game's frame rate, Windows "Hardware-accelerated GPU scheduling").

### Fixed
- The log no longer fills with one "speed=1x" warning per second while recording or streaming.

## 4.5.0 – 2026-10-10

### Added
- **See your viewers and who just came in – on every platform, in the app and on your phone.** The chat panel shows the viewers of Twitch, Kick, TikTok LIVE and now also **your YouTube live stream** (with YouTube connected), plus the total. New **“New” strip** under it: everyone who came in, newest first – people who **joined your Twitch chat or your TikTok LIVE**, and on every platform anyone who **writes for the first time this stream**; click it for the whole list with their first message. In the chat, *→ name joined* lines (hide them with the people button) and **NEW** / **FIRST TIME** tags (Twitch: their very first message in your channel). The **status bar** always shows the total viewers and the latest arrival – also with the chat closed; click it to open the chat. The **phone remote** has the same bar on top of every page: viewers per platform, the latest arrival, tap for the list. Everyone counts once per stream; bots and the people already in chat when FabStream connects are left out. Kick and YouTube have no join events – there it is the first message.

## 4.4.0 – 2026-10-09

### Added
- **VALORANT in the Auto-Cutter:** *Settings → Games → VALORANT* → switch it on. While you play, FabStream reads your own match from the Riot Client on your PC – **won rounds** and the **match result** become game events the moment they happen, and the Games page shows the map and the live score. **Connect your Riot account** once on the same page, and a minute after every match FabStream adds **every kill, first bloods, knife and ultimate kills, double/triple/quadra kills, aces, kill streaks (3, 5, 7, 10 … kills without dying, across rounds), clutches (1v1 to 1v5 – you as the last one alive and your team wins), spike plants and defuses, team aces** – lined up to the second with your recording, also with recordings that already ended. The Auto-Cutter ranks them (ace and clutch 1v3 first) and labels them (*Clutch 1v3*, *Kill streak ×7*, *Quadra kill* …); the Games page shows your last match (score, kills, deaths, headshots, moments) and has *Check now*. Part of Premium and up. The data comes from Riot's official match data – FabStream never sees your Riot password, and other players' names never reach FabStream.

### Known issues
- **VALORANT kills, aces and clutches need Riot's approval of FabStream** (official match data). Until then *Connect Riot account* says it is not available yet; won rounds and the match result from the Riot Client work already.

## 4.3.0 – 2026-10-09

### Added
- **Moderate Twitch and Kick at the same time** in the *Moderator Studio*: open a Twitch channel and a Kick channel (yours with *My channel*, or any channel you are a moderator of) – both chats run in one list, every line marked **T** or **K**. Delete, time out and ban from the line, open the user card (timeouts, ban, unban – warnings on Twitch), and write to both chats at once or choose *Twitch* / *Kick* next to the chat box; */timeout*, */ban* and */unban* work for Kick too. The stream card shows both streams. Kick allows timeouts up to 7 days; its chat modes and announcements have no API and stay on kick.com. **Connect Kick once more** (*Settings → Accounts*) so FabStream gets Kick's moderation permissions. Part of Ultra and Max.
- **Sign in on the phone with a QR code:** *Settings → Remote control → Phone or tablet* → *Show QR code*, scan it with the phone's camera – the remote opens and signs in by itself and remembers it. The code holds the password, so it stays hidden until you ask for it and hides itself after 2 minutes; the password never leaves the phone over the network.
- **Post clips straight to TikTok:** sharing a clip to TikTok (clip library or Auto-Cutter) now opens a *Post to TikTok* window: it shows the TikTok account the post goes to and a preview, you write or edit the caption (hashtags and @mentions work), choose **who can see it** (Everyone, Friends, Followers or Only me – nothing is preselected), allow **comments, Duet and Stitch** if you want (all start off; options you switched off in TikTok stay greyed out) and, if the clip promotes something, **disclose commercial content** (*Your brand* or *Branded content*, with TikTok's label). Press *Post* and FabStream uploads and publishes it – it may take a few minutes until it is visible on your profile. Prefer to finish in the TikTok app? *Send to drafts instead* works like before. In the Auto-Cutter every clip gets its own window.

### Improved
- **Layouts you can rearrange – Auto-Cutter and Moderator Studio:** drag an area by its grip (⠿) to another place and the others slide aside – in the Auto-Cutter the recordings list and the clip details to the other side (the editor keeps its order; drag the line under the previews to make them bigger or smaller); in the Moderator Studio the three columns and every card (stream, chat modes, shield, announcement, user, log) can be moved, also into the other side column. All dividers resize, the layout is remembered, arrow keys on a grip move it too, and *Reset layout* (layers icon) brings the default back.

### Known issues
- **Connect TikTok once more** (Clips → Upload → TikTok) to allow posting – connections made before 4.3 can only send to drafts.
- Until TikTok has approved FabStream for public posting, posts can only go to **private TikTok accounts** and are visible to you only. Sending to drafts is not affected.

## 4.2.0 – 2026-10-09

### Added
- **Moderator Studio** – a new tab at the top: moderate your own Twitch channel or any channel that made you a moderator, straight from FabStream. Pick the channel (live ones first), see the stream (title, game, viewers, uptime) and the live chat. Delete a message, time out or ban with one click on the line; click a name for the user card (messages this session, account age, timeouts from 1 minute to 7 days, warn with a reason, ban, unban). Switch slow mode, followers-only, subscribers-only, emote-only and unique chat, turn on **shield mode** during a hate raid, clear the chat, send **announcements** – and type Twitch's slash commands (*/timeout name 10m*, */ban*, */unban*, */warn*, */slow*, */followers*, */clear*, */announce* …). The log shows what you and the other moderators did. Connect Twitch once more (*Settings → Accounts*) so FabStream gets the moderation permissions. Part of **Ultra and Max** (and the 7-day trial).
- **Phone remote with more pages:** swipe left and right (or tap the tabs): **Chat** – read every platform's chat and write to Twitch / Kick; **Bot** – switch FabBot on and off, post a command's answer, send a timed message, say something as FabBot, run **polls** and **giveaways**; **More** – show or hide each source separately in 16:9 and 9:16, every hotkey action as a button, CPU / frame rate / dropped frames. The remote now has its own icon – also when you add it to your phone's home screen.
- **Ultra short clips (5–10 s)** in the Auto-Cutter (*Clip length*) – for Shorts and TikTok hooks.
- **Legend under the Auto-Cutter timeline:** what every mark means (game event, your voice, loud sound, chat, follow / sub / raid, your marker, big change on screen) with how often it occurs.
- **Drag & drop you can see:** when you drag a scene or a source, it moves into place while you drag, the others slide aside, and a short glow shows where it landed. Scenes can now be dragged too.
- **Recording names say what they are:** date, time, resolution and frame rate, e.g. *FabStream_landscape_2026-10-09_16-16-05_1920x1080_60fps.mp4*. The Auto-Cutter shows them as *FabStream · 09.10.2026, 16:16 · 1920×1080 · 60 fps* – older recordings get resolution and frame rate read from the file.
- **Games:** the ten most played games are prepared next to BeamNG.drive and VALORANT (Counter-Strike 2, League of Legends, Dota 2, Fortnite, GTA V, Minecraft, ARC Raiders, Overwatch 2, World of Warcraft, AION 2) – shown as *Coming soon* with what FabStream will find in each.

### Improved
- **Plans are checked by the FabStream server too:** the Moderator Studio and sharing clips only work when the server can see Ultra or Max – on your account, or on this PC (also for plans bought with a license key that is not linked to your account). If the server says no, FabStream shows the plans.
- **Plans:** platforms per format **Free 1 · Premium 2 · Ultra 4 · Max 8**; resolution and frame rate **Free 1080p 60 fps · Premium 1080p 120 fps · Ultra 1440p 240 fps · Max 4K 240 fps**; PCs per license **Premium 1 · Ultra 3 · Max unlimited**. The **Mixer** (with separate audio tracks), **remote control** (Stream Deck, Touch Portal, phone) and the **Auto-Cutter** are part of Premium and up, the **Moderator Studio** of Ultra and up – without them they show what they do and lead to the plans. Existing subscriptions get the limits of the new plans. Free needs no account. Settings from a bigger plan are brought back into yours (e.g. Premium at 1440p goes to 1080p).
- **7-day trial with a free account:** *Try it free for 7 days* asks you to create a FabStream account (or sign in) – no credit card. There is one trial per account (also across linked sign-ins, e-mail addresses and PCs); when it ends, FabStream asks you to choose a plan and otherwise continues as Free. Trials started before 4.2 run out as they were.
- **Assistant measures more exactly and says where:** every test runs at least 5 seconds; download and upload use two connections and leave out the warm-up. Ping is measured as real network round trips (no server time in it) to the FabStream server **and every streaming server you switched on** (Twitch, YouTube, Kick …) – *Where it was measured* shows each server with address, location, ping, jitter, loss and number of samples. The Ping tile shows the slowest streaming server.
- **Website:** plans, prices table, FAQ and terms show the new plans and the trial; a new *Moderator Studio* section.
- **Security: FabStream only runs as delivered.** The app's program files are now one sealed package whose fingerprint is stored in *FabStream.exe* – if anything changes them on your PC (malware, a broken copy), FabStream refuses to start instead of running altered code. Reinstalling fixes it.
- **Security: you are told when your sign-in e-mail changes.** If FabStream support changes the e-mail address of your account (e.g. on your request), the old address gets a notice – so a change you did not ask for never goes unnoticed.
- **Fair trial – one per streamer:** the 7-day trial now needs your **Twitch account or YouTube channel, at least 30 days old** (connect it right from the trial button – *Connect Twitch* / *Connect YouTube*), and every channel gets one trial. It is started in the app only, and *name+anything@…* or Gmail addresses with extra dots count as the same address. Kick alone cannot be used for the trial – Kick does not share how old an account is.
- **Website:** the public status check no longer shows which services are set up (that is in the admin tool now).

### Fixed
- **BeamNG.drive: a hard landing after a big jump is no crash any more.** Crashes now look at the *forward* speed and a *sideways or frontal* knock only – landing stops the fall but the car rolls on, so it is a *Big jump*. A landing that ends nose-first in the ground or a wall still is a crash.

### Known issues
- The Moderator Studio moderates Twitch channels; Kick follows later. The stream itself opens on Twitch (*Watch on Twitch*) – inside FabStream you see the live picture, refreshed every minute.
- The other games in *Settings → Games* are prepared, not usable yet.

## 4.1.0 – 2026-10-09

### Added
- **Recordings sorted by format:** new recordings go to **Horizontal** (16:9) and **Vertical** (9:16) inside your recordings folder, clips to *Clips → Horizontal / Vertical*. Older recordings stay where they are and still show up in the Auto-Cutter and the library.
- **Settings made simpler:** the menu is grouped (Basics, Picture & sound, Output, Control, Accounts, System). *Remote control* and *Games* are now big switches and a button per device or game – behind each button short steps with the values to copy (address, port, password); port and new password sit under *Advanced*. *Account* is now *Accounts*.
- **Save keeps the settings open:** *Save* shows "Saved" and you can keep going; *Close* closes the window. The settings window is bigger.

### Improved
- **Website:** the comparison guide is now *FabStream vs. other streaming platforms* (the old address forwards to it).

### Fixed
- **BeamNG.drive: full braking is no crash any more.** A crash is now a real impact on the car body (MotionSim: a fast loss of speed together with a hard knock) – full braking, also with locked wheels, never counts.
- **Game Capture is smooth:** while a game is captured, FabStream no longer asks Windows for every capturable window every 2 seconds (that made the picture stutter) – it only checks which window is in front. The capture runs at a steady frame rate.
- **No black flashes in Game Capture:** while a game shows a black screen (loading, switching modes) the last real picture stays on screen, for up to 20 seconds.
- Settings pages could slide under the *Cancel / Save* buttons in smaller windows.

### Known issues
- BeamNG crashes need *MotionSim* switched on in BeamNG (OutGauge alone has no data about the car body).

## 4.0.0 – 2026-10-09

### Added
- **Game events for the Auto-Cutter – BeamNG.drive:** switch it on in *Settings → Games* and turn on *OutGauge* and *MotionSim* in BeamNG (*Options → Other*, IP 127.0.0.1, the port FabStream shows). While you record, FabStream notes **crashes (with the speed), rollovers, big jumps and top-speed runs**, and the Auto-Cutter turns them into highlights such as *Crash at 94 km/h* – even when you stayed quiet. The settings show live whether BeamNG is sending data. *What counts* has a new *Game events* switch.
- **Mute and solo every audio track in the Auto-Cutter:** each track (A1 Mix, A2 Mic, A3 Game …) has **M** and **S** like in a video editor. Mute Discord, solo your voice – the preview plays exactly that, the transport shows what the clips will sound like, and every clip is cut with that sound (one track is copied as it is, several are mixed).
- **YouTube Shorts with every important setting:** visibility, **scheduled publishing** (the first clip at a time you choose, then one every 1–48 hours), category, audience (made for kids or not), video language, *Notify subscribers*, the *Altered or synthetic content* label, license, embedding and **adding the Short to one of your playlists**. FabStream remembers your choice; replay clips you upload from the Studio use it too. A clip that would not become a Short (no 9:16 file, longer than 3 minutes) says so before you upload.
- **Resize the Mixer and Auto-Cutter like the Studio:** drag the edge of the insert panel, the recordings list, the previews and the clip details. Arrow keys move an edge, a double-click resets it; FabStream remembers the sizes.
- **Website: new language menu** with flags – English, Deutsch, Italiano – on every page.

### Improved
- **Website search results:** the sign-in page no longer shows up in Google, and the descriptions of the license and Italian download pages fit fully into the search results.

### Fixed
- Two Auto-Cutter cuts in the same second could give their clips the same file name; a new clip now never replaces an existing one.

### Known issues
- VALORANT kills are not detected yet: Riot offers no live event interface, so FabStream will read them from the recording's picture – this needs tuning with real recordings first.
- Tracks muted in the Auto-Cutter only work with recordings that have separate audio tracks (*Settings → Recording*); for older recordings the lanes show the levels only.
- Muting or soloing a track replaces the mix with the separate tracks that are on – sound without a track of its own (an insert without REC) is then left out.

## 3.10.0 – 2026-10-09

### Added
- **Auto-Cutter timeline like a real video editor:** below the previews the recording is now laid out in tracks – **V1 16:9** and **V2 9:16** as filmstrips with frames from your video, then **A1 Mix** and **one lane per separate audio track** (e.g. *A2 Mic*, *A3 Game*, *A4 Discord*), each with its own waveform and name on the left. You see at a glance whether you, the game or Discord was loud, and the highlight markers run across every track. Recordings without separate tracks show the mix; 3.8 recordings show the levels FabStream noted while recording.
- **Right-click on a mixer channel:** rename, *Add plugin* straight into the next free slot, effects, mute, solo, REC, fader to 0 dB, pan to centre, route a source here, the source's filters, move to another insert or reset. The master has its own menu.

### Improved
- **The Mixer fills the whole window:** the channels share the full width instead of sitting on the left.
- **Mixer and Studio stay in sync:** an insert with one source uses that source's volume and mute – move the fader in the Mixer tab and the Studio audio mixer follows, and the other way round.
- **New sources get their own insert:** once you use the mixer, a newly added audio source goes onto the next free insert by itself.
- **Engineering page moved to the FabStream website:** *How FabStream is built* (privacy, security, measurements) now lives on fabstream's own site; old links forward automatically.
- **Website:** new sections with real screenshots of the **Mixer** and the **Auto-Cutter**, and fresh screenshots of the app everywhere else.
- **Smaller download page:** the release only offers the installer – the portable ZIP is gone.

### Known issues
- Filmstrips of very long recordings use key frames only, so neighbouring frames can look alike.

## 3.9.0 – 2026-10-09

### Added
- **Mixer tab – like FL Studio, only simpler:** a new tab between *Studio* and *Auto-Cutter* with a **master and 16 inserts**. Send each audio source to an insert (*One insert per source* does it in one click), and every insert gets **10 plugin slots** with the built-in effects (EQ, compressor, noise gate, limiter, de-esser, expander, warmth, game EQ, stereo width, delay …), a **fader, pan, mute and solo**, plus live meters. The master has its own slots too – e.g. a limiter on everything your viewers hear.
- **Separate audio tracks in recordings:** switch on *Settings → Recording → Separate audio tracks* and press **REC** on up to 5 inserts. Every recording then has track 1 = the full mix plus one track per REC insert (e.g. *Mic*, *Game*, *Discord*), named after the insert – so you can cut, mute or level your voice, the game and Discord separately in Premiere, DaVinci Resolve or CapCut. The tracks stay sample-exact with the picture. Your stream is not affected: platforms always get the mix. Replay clips keep the tracks too.
- **Control FabStream with your Stream Deck and other control apps:** Elgato Stream Deck, Touch Portal, Streamer.bot, Loupedeck, Bitfocus Companion and other remote apps work without anything extra: switch scenes, go live, record, mute and set volumes, show and hide sources, studio mode and transition, replay buffer and *Save clip*. Switch it on in *Settings → Remote control*; it shows the password and what to enter in each app.
- **Both formats from one button – or each on its own:** *Stream* and *Record* on the Stream Deck use every format you set up. The outputs **stream 16:9**, **stream 9:16**, **record 16:9** and **record 9:16** start and stop one format alone. *Trigger hotkey* runs every FabStream shortcut by name (e.g. `FabStream.markMoment`).
- **Phone remote:** with *Allow phones and tablets in my network* on, open the address shown in the settings on your phone (same Wi-Fi), enter the password and you get the live picture (16:9 or 9:16), *Go live* / *Record* with the running time, separate buttons for each format, scenes, the mixer with mute and volume, *Mark moment*, *Save clip*, the replay buffer and studio mode. Nothing to install.

### Improved
- **Coming soon – Cloud Relay:** the pricing on the website announces it: your PC sends each format only once and our server forwards it to all your platforms, so 3 + 3 destinations need about 12 Mbit/s upload instead of 36. It will be included in Max and available as an add-on for Premium and Ultra; streaming directly from your PC stays the default. Nothing to buy yet.
- **Two new guides on the website:** *How to stream to TikTok and Twitch at the same time* (step by step, from the stream keys to the TikTok safe zones) and *Vertical streaming: FabStream vs. other streaming platforms* – in English, German and Italian, linked in the footer of every page.
- **Easier to find on Google:** the website's home page title and description now say what FabStream is – free streaming software that streams 16:9 and 9:16 at once.
- **Safe by design:** the remote control is off until you switch it on, always needs the password (stored encrypted on your PC; *New password* signs every connected app out), only accepts apps on this PC unless you allow your home network, never accepts connections from the internet, and pauses an address for a minute after 5 wrong passwords.

### Known issues
- The plugin slots use FabStream's built-in effects; external VST plugins can't be loaded yet.
- Separate tracks work in MP4 and MKV recordings (FLV holds one audio track). Sound from video files in your scenes is part of the mix only. Clips cut in the Auto-Cutter and in the recordings library keep the mix.
- *Solo* on an insert also changes what your stream hears – it's meant for checking a source quickly.
- Another streaming program may use the same port (4455). If it runs at the same time, choose another port in FabStream (*Remote control → Advanced*, e.g. 4456); FabStream tells you when the port is taken.
- Remote apps can switch and control things but can't yet create or rename scenes and sources, change filters or pause a recording. Pictures are available of the live scene (and the preview scene in studio mode), not of single sources.

## 3.8.0 – 2026-10-09

### Added
- **The Auto-Cutter understands what happens – not just what is loud:** a highlight now comes from several signs together: **your voice**, **chat going wild**, **raids, donations, subs and follows**, **your markers and saved clips** and **big changes on screen** (death screen, explosion, kill cam). Game sound that simply gets louder is no longer a highlight on its own – only when another sign comes with it. Every highlight says why it was picked ("You reacted · Chat went wild"), and the signs appear as coloured dots on the timeline.
- **Choose exactly which sound counts:** *Auto-Cutter → What counts* lists every audio source of the recording – microphone, game or desktop sound, Discord, music – each with **Strong** (enough on its own), **Counts** (only together with another sign) or **Off**. Switch the other signs on or off too. FabStream remembers your choice for the next recording.
- **Recordings keep their sources apart:** while you record, FabStream notes the level of every audio source, chat activity, stream events and your markers (a few MB for hours, stored on your PC) – so the Auto-Cutter can tell your shout from a loud game.

### Known issues
- Recordings made before 3.8 only have the mixed sound: there the Auto-Cutter uses all sound together plus the picture. Chat, events and markers are available for new recordings.

## 3.7.1 – 2026-10-08

### Fixed
- **Sound late in the stream:** viewers heard the sound up to about half a second after the picture. Desktop and application audio (game, Discord, music) built up a delay after every quiet moment and after short busy phases of the PC – the delay now stays at a few hundredths of a second, also in long streams. The mixer also runs with smaller audio buffers, so the microphone reaches the stream sooner.

- **Recordings stay safe while they run:** the Auto-Cutter no longer lists a recording that is still running (it appears as soon as you stop it), and FabStream never prepares a file that is still being written. If FabStream or the PC is closed while a recording is being prepared, the recording is put back in order on the next start – nothing is lost, and half-finished copies don't show up in your recordings.

### Added
- **Audio sync:** *Settings → Audio → Audio sync* moves the sound earlier (or later) in streams and recordings, in 10-ms steps up to one second – for setups where a device itself is slow (e.g. some wireless headsets or capture cards). Applies the next time you go live or record.

### Improved
- **Smooth playback in the Auto-Cutter:** video and sound of a recording no longer stutter in the editor. The 9:16 preview now follows the 16:9 one smoothly instead of jumping to catch up, and the studio behind the tab rests (only a few frames per second) while nothing records, streams or buffers – the status bar shows *Studio resting*. As soon as an output runs, the studio renders at full speed again.
- **Recordings jump to any moment instantly:** FabStream records crash-safe MP4 files, which players can only search slowly. After a recording ends (once nothing records or streams any more), FabStream now adds a seek index to the file – in seconds, without re-encoding and without changing the picture or sound. Recordings you made before are prepared the first time you open them in the Auto-Cutter ("Preparing the recording for smooth playback"). If a file can't be prepared, it stays exactly as it was.

## 3.7.0 – 2026-10-08

### Added
- **Auto-Cutter gets its own tab:** next to *Studio* in the top bar. On the left are your **recordings** (one entry per stream, 16:9 and 9:16 together, with their length) and your **clips**. The studio keeps running in the background – your stream and recording go on while you cut.
- **Browse all your clips:** the *Clips* side shows every clip as a card with a preview that plays when you point at it. The 16:9 and 9:16 file of a moment are one card. Filter by format and by where it came from (Auto-Cutter, replay buffer, cut by hand), search and sort (newest, oldest, longest). Click a clip to watch it in both formats, see its details, show it in its folder, delete it (both formats, recycle bin) or share it. Tick several clips to share them in one go.

### Improved
- **The film icon next to *Save clip*** now opens your clips in the Auto-Cutter tab.
- **App tour:** a new step shows the Auto-Cutter tab.

## 3.6.0 – 2026-10-08

### Added
- **Auto-Cutter – your stream's best moments as clips:** open *Outputs → Auto-Cutter* (or the wand next to a recording in *All recordings*). FabStream listens to the recording and marks its highlights – loud reactions, cheering, the big plays – on a timeline with the waveform, right under **two previews: 16:9 and 9:16** of the same moment, kept in sync (FabStream lines the two recordings up by their sound). Choose how picky it is (*Only big reactions / Normal / Many highlights*) and the clip length (short for TikTok and Shorts, longer for YouTube).
- **Edit the highlights like in a video editor:** drag a marker to move it, drag its edges to make it longer or shorter, type exact times, add your own (*Add highlight*, double-click the timeline or **N**) and remove the ones you don't want (**Del**). Play a highlight in a loop, zoom the timeline (**Ctrl + mouse wheel**), **Space** plays, **I / O** set start and end at the playhead. Per highlight you choose the formats to cut – 16:9, 9:16 or both.
- **One click cuts every clip:** *Cut* turns all highlights into clips in their formats at once – fast, without re-encoding, straight into your clip library. **Cutting needs Premium**; finding and editing highlights is free.
- **Share to all platforms at once:** after cutting, give each clip a title, a description and hashtags (plus hashtags for all clips), tick YouTube and/or TikTok and press *Share*. YouTube gets the 9:16 file as a **Short** with your title, description and hashtags as tags; TikTok gets it in your inbox and FabStream copies the caption for you. Progress and the link to every upload show right next to the clip. **Sharing needs Ultra.**
- **The 7-day trial includes the Auto-Cutter** with cutting and sharing.

### Improved
- **YouTube uploads with tags:** clips you upload to YouTube now carry your hashtags as video tags.
- **Clip upload is part of Ultra:** uploading clips from the clip library to YouTube Shorts or TikTok now needs Ultra (or the trial), like sharing from the Auto-Cutter. Saving, cutting by hand and playing clips stay free.

### Known issues
- A recording whose video the app cannot play (rare formats) shows no preview picture – the timeline, cutting and sharing still work. Recordings without sound get no automatic highlights; add them yourself.

## 3.5.3 – 2026-10-08

### Improved
- **Faster help from the FabStream team:** our support team now has its own support tool – your bug reports and ideas are tracked until they are handled, and whoever helps you sees the notes of earlier conversations, so you don't have to explain everything again.

### Fixed
- **Plans can only be bought with real payments:** while our payment system is still being tested, the website and the app's *Buy* button show "purchases open soon" instead of a test checkout – before, a test payment could unlock Premium, Ultra or Max. Licenses you already have keep working until real sales start.
- **Safer admin access:** the website's admin tool can only be opened by the personally named administrators, no longer by the shared support mailbox.

## 3.5.2 – 2026-10-08

### Improved
- **New website:** fabstream.fabcomstudios.com has a new home page with fresh screenshots of the current app – the editor with both formats, the built-in alerts and widgets, Go Live to several platforms, voice presets, scene presets and FabBot – plus a clearer download page and a new preview picture for links shared on social media. In English, German and Italian.
- **Scene from a preset:** the last preset card now fills its row instead of sitting next to an empty space; the same goes for the other card lists in the app.

### Fixed
- **StreamElements shows "Connected":** after connecting, the toast said connected but *Widgets → Donations & follows* kept showing "Not connected" when the Widgets tab was opened before the Chat tab. The row now shows the real state right away (Connecting… → Connected, or the error).

### Removed
- **Streamlabs:** the Streamlabs donation connection is gone again – connect **StreamElements** for tips, YouTube members and Super Chats (Twitch follows still come straight from Twitch). A stored Streamlabs token is deleted from your PC on the next start. Overlay links of any service still work as a browser source.

## 3.5.1 – 2026-10-08

### Fixed
- **Game Capture finds your game when you switch to it:** *Capture any game automatically* used to know games only by a list of titles, so many games were never picked up – also after Alt+Tab. It now looks at the program behind each window: games from Steam, Epic, Riot, Xbox, GOG, Ubisoft, EA and Rockstar folders, Unity / Unreal / GameMaker / Godot games and any fullscreen program you switch to are recognised, and the game you Alt+Tab to wins. When you look at something else (browser, Discord …), the capture stays on your game.
- **Never browsers, FabStream or other apps:** browsers (also in fullscreen), FabStream itself, launchers (Steam, Epic, Battle.net, Riot Client …), Discord, other streaming programs, video players, editors and Windows windows are never taken as a game. The game picker marks the detected games and lists them first.

### Known issues
- A game in exclusive fullscreen can still show black – switch it to borderless / windowed fullscreen. A game that is neither in a known folder nor fullscreen is found when you pick it in *Choose game…*.

## 3.5.0 – 2026-10-08

### Added
- **Game Capture:** *Sources → + → Game Capture* records your game directly. Choose **Capture any game automatically** – FabStream takes the known game that is running (Fortnite, VALORANT, Minecraft, CS2, League of Legends, Apex and many more), waits while none is open and moves on to the next game you start – or pick the game window yourself (known games are listed first). When the game restarts, FabStream finds it again by itself. Nothing is injected into the game, so anti-cheat is not affected; games in exclusive fullscreen may show black – switch them to borderless or windowed fullscreen.
- **Scene presets:** *Scenes → + → Scene from a preset…* (or straight from the menu) adds a ready-made scene for 16:9 and 9:16 at once: **Starting soon** (title, 5-minute countdown, chat), **Gaming** (Game Capture, webcam, alerts, goal bar, chat in 9:16), **Just Chatting** (big webcam, chat, event list, latest donation), **Be right back** and **Ending** (thank-you title, recent supporters, top donation). Everything in it is a normal source you can move, change or remove. Timers start when you press start in their properties.
- **App tour in English, German and Italian:** a short guided tour lights up each part of the window – scenes, sources, the two canvases, audio mixer, Go Live, chat & widgets, account – and explains it. It starts once (also once after this update), can be skipped at any step and is then not shown again. Watch it again any time: *profile menu → App tour*.
- **Streamlabs is back for donations:** *Widgets → Donations & follows → Streamlabs → Connect* opens your Streamlabs API settings – copy **Your Socket API Token** and FabStream picks it up and connects by itself (pasting works too). Streamlabs tips, follows, YouTube members and Super Chats then show up in Activity, alerts, goals and labels, next to StreamElements if you use both. The token is stored encrypted on your PC only.
- **Admin badge:** FabStream team accounts get a gold *Admin* badge in the app (profile) and on the website, with a direct link to the admin dashboard.

### Improved
- **The preview's left and bottom edges can be dragged too:** like the divider to the side panel, you can now drag the edge between the scenes / sources column and the preview, and the edge between the preview and the audio mixer / outputs row. FabStream remembers the sizes; double-click an edge for the default. The preview always keeps enough room, and its toolbar stays on one line when it gets narrower.
- **Admin dashboard (FabStream team):** a clearer layout with grouped navigation, a search over all accounts and licenses (Ctrl+K), key figures with trends, 30-day charts for sign-ups, subscriptions and downloads, and a list of what needs attention (open payments, licenses ending soon, new bug reports, licenses without an account). New pages for feedback, app versions in use, top inviters and system status, plus tools: extend a license by 7 / 30 / 365 days, send a test e-mail, export accounts and licenses as CSV.

## 3.4.1 – 2026-10-08

### Fixed
- **StreamElements connects:** saving the JWT token stopped with "invalid secret id" even with the right token. The token is now stored (encrypted, as before) and StreamElements connects – paste or pick it up again in *Widgets → Donations & follows*.
- **TikTok LIVE chat:** the same error stopped saving the TikTool API key in *Chat → ⚙*; it is stored now.

## 3.4.0 – 2026-10-07

### Added
- **Settings → Assistant – what your PC and connection can really stream:** one click measures upload, download, ping, jitter and packet loss to the FabStream server, finds your hardware encoder and reads CPU threads, memory and graphics card. Then every quality from 720p30 to 1440p60 is rated for the destinations you switched on – *Great*, *Fine*, *Tight*, *Too much* or *not in your plan* – with the reason (e.g. "Twitch takes max. 6 Mbit/s"). *Use recommended settings* (or pick any other row) fills in resolution, frame rate, bitrate and encoder for 16:9 **and** 9:16; *Save* keeps it. The quick auto-configuration in *Settings → Video* is still there (*Quick setup…*).
- **Game & sound presets for game and desktop audio:** *Audio Mixer → ⋮ → Game & sound presets…* on Desktop Audio or an application offers six complete chains – *Cinematic*, *3D Surround*, *Competitive – Footsteps*, *Story & Dialogue*, *Punchy Arcade* and *Background Bed*. They widen or narrow the stereo image (with the bass kept in the centre), shape the sound and leave a **"voice pocket" around 3 kHz**, so your microphone always sits on top of the game. The mixer shows which preset a channel uses; the preset dialog has a *Voice* and a *Game* tab (*Filters → Presets* too).
- **Stream tags:** the *Title* editor of Twitch, Kick and YouTube (Outputs & Streaming, Settings → Stream) now shows the channel's current tags as chips – type and press Enter or comma to add one, × removes it. FabStream cleans them the way each platform accepts them (Twitch: letters and digits only, up to 10; Kick: up to 10; YouTube: up to 500 characters together) and saves them together with title and category.
- **TikTok LIVE chat, gifts and follows:** enter your TikTok name in *Chat → ⚙* and FabStream shows your TikTok LIVE chat next to Twitch and Kick, with gifts (one alert per gift combo, e.g. *"Mo sent 7× Rose (7 💎)"*), follows, subs and the viewer count (also in the viewer chips of the Chat tab). TikTok gifts work in alert boxes, the event list, labels and goal bars (*Bits / TikTok diamonds*, goal platform *TikTok*), and TikTok viewers can vote in FabBot polls and join giveaways. TikTok has no public chat API, so this runs through the **TikTool LIVE** service with **your own API key** (tik.tools – 7 days free, then from $19 a month; the key is stored encrypted on your PC). FabBot and the chat field cannot write in the TikTok chat, and TikTok viewers are not part of *Total viewers* yet. **Beta.**
- **Background music with your own playlist:** *Audio Mixer → Add Audio → Background music* creates a *Music* channel that plays your own local songs into the stream and recordings – add single files, a whole folder (with sub folders) or **import a playlist from Windows Media Player** (.wpl) or any M3U / PLS playlist (VLC, Winamp, foobar2000). Shuffle, repeat all / one / off, start automatically with FabStream; play / pause / next / previous and the running track right in the mixer, with its own volume (starts at −12 dB so it stays under your voice), mute, filters and monitoring. A new **Now playing** label (*Widgets → Label*) shows the current song on stream. Plays MP3, M4A/AAC, FLAC, WAV, OGG and Opus (WMA files are left out). Only use music you have the rights to stream.
- **Windows Media Player as its own audio channel:** *Add Audio → Application Audio* now offers Windows Media Player, Windows Media Player Legacy, Spotify, VLC, iTunes/Apple Music, foobar2000 and AIMP even while they are not playing – FabStream picks the sound up as soon as they play, with its own fader (Windows 10 2004 or newer).

### Improved
- **Go Live picker shows what is missing:** every destination says *Ready*, *No stream key*, *No server* or *Plan limit*; Twitch, Kick or YouTube without a destination in that format are listed below with the reason and the one click that fixes it (*Connect*, *Add*, *Reconnect*). On a plan with one platform per format you pick which one goes live, and the upgrade is offered right there.
- **Account problems are visible before you go live:** FabStream checks connected Twitch, Kick and YouTube accounts in the background. If a platform rejects the connection (e.g. access was revoked or live streaming is not enabled on the YouTube channel), *Outputs & Streaming* and the Go Live picker show **Account problem** with the platform's message and a *Reconnect* button.
- **Voice presets made to sit on top of the game presets:** levels and presence are tuned so voice and game never fight. *Cinematic Podcast* is now called *Deep Podcast* and *Gaming – Noisy Room* is *Noisy Room – Keys & Fans* (channels that use them keep working and show the new name).

## 3.3.1 – 2026-10-07

### Fixed
- **YouTube: connecting works when your channel belongs to another Google account** (a brand account or a second Google account). Before, FabStream stopped with "Another Google / YouTube account is linked already – unlink it first". Now the connected Google account replaces the one that was linked before.

### Improved
- **Disconnect a platform right in Outputs & Streaming:** the small × next to a connected Twitch, Kick or YouTube removes the connection (after asking). Your destinations and stored stream keys stay.

## 3.3.0 – 2026-10-07

### Added
- **Viewers at a glance in the Chat tab:** every channel shows how many people are watching right now (Twitch and Kick), and **Total viewers** adds up all live channels – hover it for the peak since FabStream started. Offline channels say "offline". Updated every minute.
- **Platforms in Outputs & Streaming:** Twitch, Kick and YouTube side by side, each with the same options once connected – **Title** (stream title & category), **Key/Add** (fetches your stream key into the destination, or adds the platform with its key) and, for YouTube, **Chat** (opens your live chat). Not connected yet: one click on **Connect**.

### Improved
- **Every chat line names its platform:** a coloured pill (Twitch, Kick, YouTube, StreamElements) next to the dot, so mixed chats are easy to read.
- **YouTube connection:** if Google's consent page left the YouTube permissions unticked, FabStream now says so (Settings → Stream and Outputs & Streaming) and offers **Allow** to connect again – before, YouTube silently stayed "not connected".
- Website: English pages now have their own address too (`/en/…`, like `/de/…` and `/it/…`); the bare address picks your language. Old links (apps, e-mails, bookmarks, payment pages) forward to the new addresses.

### Fixed
- Website: on the Italian pages the links to the legal texts and the privacy policy pointed to addresses that no longer exist.

## 3.2.0 – 2026-10-07

### Changed
- **Invite & earn is now a commission:** you get **20 %** of every paid subscription that starts through your link – every month it is paid (yearly plans count with a twelfth of the year). In the app (*profile menu → Invite & earn*, *Plan & License*) and on your account page you see what your commission makes **this month** and **which plan it pays for** (e.g. 5 viewers on Premium pay for your own Premium) and what is missing for the next one. Your own subscription is still billed every month as usual – invites no longer unlock free plans. A free plan you already got from the old program stays until its period ends. The commission is **paid out automatically** by our payment partner Lemon Squeezy: join its affiliate program once and paste your affiliate link under *Payout* on your account page – from then on every purchase through your FabStream link (website or app) is credited to you there.

### Added
- **Select several sources at once:** Ctrl+click sources in the preview (or in the source list; Shift+click selects a range, Ctrl+A all) – then move them together, resize them together with the handles of the box around them, nudge them with the arrow keys, or right-click to align (edges, centres), distribute evenly, center the group, change the layer order, hide, lock or remove them all.
- **Source list:** click the *16:9* / *9:16* badge of a source to show or hide it in that format, and remove a source with the bin icon right next to it.
- **Your account on the website got more:** a **profile menu** at the top of every page (your name, plan and all account sections, sign out), the **commission of the month** on the overview, a **FabStream card** with the newest version, the direct download and every PC on your account with the version it runs (*update available* when it is behind), and a new **Cloud backup** tab: see the copies of your scenes and settings the app saved, download them as a file or delete them – your PCs keep their own data.

### Improved
- **FabBot tab redesigned – and much more configurable:** a clear header shows where FabBot can write (green chip = ready; a click on an orange chip connects what is missing), and four pages: *Live*, *Commands*, *Timers*, *Mod tools*.
- **FabBot giveaways your way:** choose who can enter (everyone, subscribers, VIPs), give subscribers more luck (2×, 3×, 5× tickets), keep yourself and your mods out, draw several winners at once, let entries close by themselves after 1–10 minutes and draw automatically. The chat messages for start and winner are yours to write, with clickable variables like {prize} or {winner} and a live preview.
- **FabBot polls:** press Enter to add the next answer, pick the length with one click (30 s to "until I end it"), decide whether viewers may change their vote, and write your own start and result messages.
- **FabBot commands:** search, ready-made commands with one click (!discord, !socials, !commands, !lurk, !so, !uptime, !fabstream), and an editor per command with a preview of the answer, who may use it (everyone, subscribers, VIPs or mods) and the cooldown as quick choices. New variable {commands} lists all your commands.
- **FabBot timed messages and mod tools:** intervals and chat activity as quick choices, plus *Send now*. **Mod tools:** blocked words as chips you add with Enter.
- **Safe-zone menu stays open:** in the *Safe zones ▾* menu you can now tick several platforms in a row without the menu closing after every click, and pick **All** or **None** with one click.
- **fabcomstudios.com has an address for every language:** the English pages are now at fabcomstudios.com/en/ (like /de/ and /it/). fabcomstudios.com itself opens the page in your language, and the old English addresses forward to the new ones automatically.

### Fixed
- **No more stuttering audio while multistreaming:** desktop and application audio now goes straight to FabStream's audio engine instead of waiting behind the video work of two canvases, the audio buffer gives itself a little more room automatically if your PC gets busy (and shrinks back when things calm down), short gaps are softened instead of clicking, and the stream encoder keeps the audio in step with its timestamps. Your viewers hear smooth sound in 16:9 and 9:16 at the same time.
- **No more "disabled" next to working destinations:** it only meant a platform was left out of your last Go Live. Now each destination in *Outputs & Streaming* has a checkbox for whether it is used next time you go live, next to its key status (*key stored* / *no key*).
- The hotkey *Replay buffer on / off* now points to the right place when the replay buffer is switched off (*Settings → Diagnostics → Features*).

## 3.1.0 – 2026-10-07

### Added
- **Write in your chat from FabStream:** the *Chat* tab has a message field at the bottom. Pick where it goes – Twitch, Kick or both (click the chips) – and press Enter. If a platform still needs a sign-in or chat permission, its chip says so and connects it with one click.
- **Choose your platforms when you go live:** *Go Live* first shows all your destinations per format – go live everywhere or tick only some (e.g. only TikTok LIVE today). FabStream remembers your choice for next time. Don't want the question? Untick *Always ask* or switch it off in *Settings → General*. The *Go Live* buttons of each format ask the same way, only for that format.
- **Safe zones for every vertical platform:** next to *Safe zones* a ▾ menu lets you choose which ones you see – TikTok video, **TikTok LIVE** (host bar, rankings, live comments, gifts, comment field), YouTube Shorts, YouTube Live (vertical), Instagram Reels, Instagram Live, Facebook Reels and Snapchat Spotlight. Each platform has its own colour. Sources you move or resize now **snap to the safe-zone edges**, so text and faces land in the free area by themselves (turn it off in the same menu; Ctrl or Alt while dragging still turns snapping off).
- **Hotkeys for everything:** *Settings → Hotkeys* is grouped and covers every action – go live or record **only 16:9 or only 9:16**, replay buffer on/off, switch directly to scene 1–9, mute/unmute all audio, preview mode (both / 16:9 / 9:16), safe zones on/off and *Write in chat*. New actions start without a shortcut; your existing shortcuts stay.
- **Commission that pays for your plan:** *Invite & earn* (and *Plan & License*) now shows your **affiliate commission** from the Lemon Squeezy affiliate program: earned in total, not paid out yet, your average per month – and how much more per month you need (and roughly how many paying viewers) until the commission pays for your FabStream plan. Join the program from the same card with the e-mail of your FabStream account.

### Improved
- **Bigger, clearer side panel:** the right panel (Chat, Activity, Properties, Widgets, Bot) is wider by default and shows the names of all tabs. **Drag the divider** between the preview and the panel to make it wider or narrower – the canvas preview scales to the space that is left and everything still fits. Double-click the divider for the default width. Your width is remembered.
- **Report a problem / Suggest an idea:** FabStream no longer takes a screenshot on its own. Add one yourself if you want – pick a file, drop it on the dialog or paste it with Ctrl+V (take one with Win+Shift+S). It is shown before sending and can be removed.
- **Website:** the main button at the top is now *Account*; *Download* is in the menu and leads to the download page.

## 3.0.0 – 2026-10-07

### Changed
- **New prices:** Premium $7.99 / 7,99 € a month (59 a year), Ultra $14.99 / 14,99 € (109 a year), Max $24.99 / 24,99 € (179 a year) – with 16:9 and 9:16 at the same time in every plan. Yearly billing saves up to 40%. Subscriptions you already have keep their price.

### Added
- **FabBot – the chat bot is built in:** a new *Bot* tab on the right. **Chat polls** (viewers vote with 1, 2, 3 … or the answer) and **giveaways** (viewers enter with !join, FabStream draws a winner with a rolling animation and never picks the same viewer twice) – both with new on-stream widgets *Chat poll* and *Giveaway*. **Commands** like !discord or !uptime with your own answers, cooldowns and *mods only*; **timed messages** that only post while you are live and the chat is active; **mod tools** that keep links, CAPS, spam and blocked words out of the chat box on stream (you, your mods and VIPs are never hidden). FabBot writes in your Twitch and Kick chat as you – connect Twitch / Kick once more to allow chat messages. !fabstream answers with your invite link.
- **Recordings library:** *Outputs → All recordings* lists every recording with format (16:9 / 9:16), length, resolution, size and date – filter by format, search, play, show in Explorer or delete (recycle bin). **Cut a clip** from any recording in seconds (from/to or one click for *last minute* / *last 3 min* for a Short); the clip lands in the clip library, ready to upload to YouTube Shorts or TikTok.
- **What's new, beautifully:** after every update FabStream shows what changed since you last used it – each version as a card with *New*, *Improved* and *Fixed* sections and a timeline of all versions on the left. Open it any time from your profile menu (bottom left) → *What's new* or *Settings → About*. The update dialog shows the notes of the new version the same way.
- **Invite & earn – get your plan for free:** every FabStream account has a personal link (fabstream.fabcomstudios.com/r/YOURCODE). While **3** paid subscriptions started through it are active, **Premium** is free for you – **6** for **Ultra**, **10** for **Max**, on every PC you sign in to. Copy the link, a ready-made chat command or share it to X, WhatsApp, Telegram and Reddit from *profile menu → Invite & earn* (also on *Plan & License* and in the upgrade dialog); pick your own code like /r/YOURNAME. Your progress, link visits, sign-ups and active subscriptions are shown live – only numbers, never who bought. If someone cancels, your current free plan stays until its 35-day period ends.
- **Your account on the website:** fabstream.fabcomstudios.com/account.html now has a real sign-in (e-mail code, Twitch, Kick, TikTok, Discord or Google – the same account as in the app) and a dashboard: your plan, every license with its PCs (remove one with a click), invoices & cancellation, adding a license key, *Invite & earn* with your link and progress, your profile, linked sign-ins, where you are signed in, and deleting the account. Looking up a license key without an account still works.
- **Invite & earn on the website:** a new page explains the program (*Earn free* in the menu), the pricing section shows it, and visitors who come through a link see that a friend invited them; their purchase counts for that friend for 30 days.
- **Release notes on the website:** fabstream.fabcomstudios.com/changelog.html lists every version as a timeline with filters (*New / Improved / Fixed*), in the menu as *What's new*.
- **Auto-configuration for both formats:** *Settings → Video → Auto-configure…* (also offered at the end of the first setup) checks your graphics card, CPU and real upload speed and sets resolution, frame rate, bitrate and encoder for 16:9 **and** 9:16 together – it knows how many platforms each format streams to, so multistreaming never eats more than about ¾ of your upload. You see the recommendation next to your current settings before anything changes. The upload test sends a few MB of random data to the FabStream server; if it can't run, FabStream plans with 10 Mbit/s and tells you.

### Improved
- **A real installer:** FabStream-Setup.exe is now a proper setup wizard in FabStream's look – welcome page, license, install folder, choice of desktop and Start-menu shortcuts, progress bar and a finish page that starts FabStream and links to what's new. It speaks English, German or Italian (like your Windows), shows *Fabcom Studios* as publisher with version details, still needs no administrator rights and replaces an installed version safely. In-app updates show just a short progress window and restart FabStream. The uninstaller (*Settings → Apps*) asks whether to keep your scenes, settings and license – recordings and clips are never deleted.
- **Click the “Recording saved” message** (bottom right) to open the folder with the new video already selected. The same works for “Clip saved”.

## 2.1.0 – 2026-10-07

### Added
- **Undo and redo:** *Ctrl+Z* undoes the last change in your scenes – moving, resizing, cropping, adding or removing a source, filters, source settings and more – and *Ctrl+Y* (or *Ctrl+Shift+Z*) brings it back. Up to 100 steps; a drag counts as one step. Undo does not switch the scene you are on and is not active while you type in a field.
- **Goal bar per platform:** a goal bar can count *All platforms* or only *Twitch*, *Kick* or *YouTube* (*Properties → Platform*) – e.g. one sub goal for Twitch and one for Kick. Tips without a platform (StreamElements tips) only count for *All platforms*.
- **Text size for widgets:** a *Text size* slider (and exact value in px) in the properties of every widget – chat box, alert box, event list, goal bar, labels and timer.
- **“Add platform…” – going live on more platforms without copying addresses:** *Settings → Stream → Add platform…* shows Twitch, YouTube, Kick, TikTok LIVE, Instagram Live, Facebook Live and “Other (RTMP server)”. For Twitch, YouTube and Kick one click uses your connected account (FabStream fetches the key itself). For all others, *Open …* takes you to the right page with short steps – just click *Copy* there: FabStream picks up the copied server address and stream key by itself while the dialog is open (only text that looks like a server address or a key, nothing else from your clipboard). TikTok and Instagram start as 9:16, the others as 16:9 – you can change it. Pasting by hand still works.

### Improved
- **Clicking a source in the preview opens its properties** on the right right away.
- **Widgets fill their box instead of stretching:** when you make a chat box, event list, goal bar, label or timer bigger or smaller, the text keeps its size and the widget uses the space – a taller chat box shows more messages, and the chat fills the box all the way to the top. Widgets can be resized freely (hold *Shift* to keep the proportions) and look sharp at every output size.
- **StreamElements connects in one step:** *Widgets → Donations & follows → Connect StreamElements* opens your StreamElements channel page – click *Show secrets* and copy the JWT token, FabStream picks it up and connects by itself (pasting by hand still works).

### Removed
- **Streamlabs donations:** the Streamlabs connection is gone – use StreamElements for tips (it also reports follows and YouTube members). A Streamlabs token stored by 2.0 is deleted from your PC on the first start of 2.1. Streamlabs widget links still work as a Browser Source.

### Known issues
- TikTok only shows a stream key to accounts with LIVE access (usually 1,000+ followers), and TikTok and Instagram create a new server address and key for every stream – add them again (or edit the destination) before each stream.
- StreamElements is still **Beta**: it could only be tested with recorded messages, not with a live account.

## 2.0.0 – 2026-10-06

### Added
- **Stream widgets built in – no widget links needed:** *Add source → Stream widgets* (or the new *Widgets* tab) adds an **Alert box**, **Chat box**, **Event list**, **Goal bar** or a **Latest / top label** (“Latest donation: Anna – $5.00”, “Top cheer”, “Latest follower” …). FabStream draws them itself from your chat and activity, placed separately in 16:9 and 9:16 like any source.
- **Alert box:** pops up for follows, subs (and YouTube members), gifted subs, raids, bits and donations / Super Chats – each type on or off, minimum bits / donation / raid size, display time, slide / fade / pop animation, your own sound (through the mixer, so it is in the stream and recording only while the scene is live) and your own picture, GIF or short video. Alerts queue up one after another; *Test alert* buttons show what it looks like.
- **Donations and follows from Streamlabs or StreamElements:** *Widgets → Donations & follows → Connect…* and paste your Streamlabs “Socket API Token” or StreamElements “JWT Token”. Tips, follows and YouTube members / Super Chats then appear in Activity, in your alert box, goals and labels. The token is stored encrypted on your PC only.
- **Goal bar** counts subs (gifted subs included), gifted subs, bits, donations or follows automatically while FabStream runs – also while its scene is not on screen; the current value can be edited or reset. Test alerts are never counted.
- **Chat box on stream** in one click from the Chat tab (16:9, 9:16 or both): messages wrap, can fade out after a few seconds, and subs / gifts / raids / bits / donations can be shown in the chat.

- **Twitch follow alerts straight from Twitch:** when Twitch is connected in your FabStream account, new followers appear in Activity, in the alert box, goal bars and labels. Already connected Twitch before? *Widgets → Twitch follows → Connect again* (or Settings → Account) once to allow it. A follow that Streamlabs/StreamElements also reports is shown only once.
- **Emotes as pictures:** Twitch and Kick emotes show as pictures in the Chat tab and in the chat box on stream.
- **Own sound and picture per alert type:** e.g. a coin sound for donations and a confetti GIF for gifted subs (*alert box → Own sound / picture per alert type*); empty types use the general sound and picture.
- **Activity and labels survive a restart:** the last follows, subs, gifts, raids, bits and donations – and “Latest donation” / “Top cheer” – are still there after you restart FabStream.

- **Messages read aloud (text-to-speech):** the alert box can read donation, cheer and sub messages aloud with a Windows voice of your choice – after the alert sound, through the mixer (in the stream and recording), with minimum amount, speed, maximum length, “Name says: …” and a list of blocked words. Links and cheer words are skipped, the alert stays on screen while it speaks. *Alert box → Read messages aloud.*
- **Timer / countdown widget:** “Starting in 4:59” countdown with Start / Pause / Reset, countdown to a time of day (e.g. 20:00), stopwatch, clock or stream uptime – with your own title and end text (“Starting now!”).

### Improved
- **Right side is now one panel with tabs: Chat (open by default) · Activity · Properties · Widgets.** The chat has the full height; the source properties open when you need them – *right-click a source → Properties…*, double-click it in the source list, or right after adding a source. The open tab is remembered.
- **Activity tab:** every follow, sub, gift, raid, bits and donation with time and the viewer's message, a red counter on the tab for new events, and *Show again* to replay any of them as an alert.
- **Settings → Plan & License shows everything about your licenses:** the plan on this PC (where it comes from, key, renewal, last check), every license on your account with status, renewal or end date, monthly / yearly billing, purchase date, how many PCs use it and which ones (remove a PC with one click), *Invoices & billing*, adding a license key to your account, and the plan comparison. Before, these details were only on the *Account* page.
- Website: new feature “Alerts, chat box & goals built in” (EN/DE/IT, marked Beta); the privacy policy explains the optional donation-service connection.

### Known issues
- **Donation services are Beta:** Streamlabs and StreamElements could only be tested with recorded messages, not with live accounts yet – please report anything that does not show up.
- Twitch follow alerts need the Twitch connection of your FabStream account (Settings → Account); Kick follows are not available yet.

## 1.13.0 – 2026-10-06

### Added
- **Chat & activity panel:** your Twitch and Kick chat right in FabStream (right column, under the source properties) – no sign-in needed, just enter your channel. Subs, gifts, raids and bits are highlighted and have their own *Activity* tab. Kick chat is in Beta.
- **Chat overlay for 16:9 or 9:16:** one click in the chat panel adds a transparent chat box to the canvas you choose (as a Browser Source) – move and resize it like any source.
- **YouTube:** connect YouTube (Settings → Stream) to fill in your stream key, change the title and category of your broadcast and open your YouTube live chat in its own window.
- **Upload clips to YouTube Shorts or TikTok:** clip library → *Upload*. Vertical clips up to 3 minutes become Shorts (title, description, visibility); TikTok clips go to your TikTok drafts, where you add caption and sound in the app. The file goes straight from your PC to the platform, with progress and Cancel. YouTube allows only a limited number of uploads per day for all FabStream users together while FabStream is new – if the limit is reached, try again the next day.
- **Crop with the mouse:** hold *Alt* and drag a handle of a source to crop it (the picture keeps its size); dragging back out uncrops. Works on rotated and flipped sources.
- **Rotated sources keep their handles:** resize a rotated source along its own edges – the opposite corner stays in place.

### Improved
- Snapping while resizing is now switched off with *Ctrl* (*Alt* + handle crops); while moving, *Alt* or *Ctrl* place freely.

### Known issues
- **YouTube and TikTok connections need the platforms' approval of FabStream.** Until Google and TikTok have reviewed FabStream, *Connect YouTube* / *Connect TikTok* may show an error for most accounts.
- Kick chat uses Kick's own chat connection and may stop working when Kick changes it (Beta).
- Twitch follows are not shown in the activity list (Twitch only shares them with a signed-in connection).

## 1.12.0 – 2026-10-06

### Added
- **Buy or upgrade a plan directly from the app:** *Upgrade* now has a monthly/yearly switch and one button per plan. The payment page opens straight away (no detour over the pricing page) with your e-mail already filled in; the purchase is bound to your FabStream account. While you pay, the dialog shows "Waiting for your purchase…" and the plan switches on by itself the moment the payment arrives – no license key to copy. Not signed in yet? You sign in once first (e-mail code, Twitch, Kick, …). *Buy without an account* still exists.

### Improved
- **Profile button moved to the bottom left** (under the sources); its panel opens above it.
- **Filters dialog:** wider, filter names no longer wrap or overlap – the voice preset ("Cinematic Podcast") is shown small above the filter name, the move/remove buttons appear on hover and on the selected filter, the header buttons stay on one line and the level meter uses the full width.
- Upgrade dialog: the price row of the plan table follows the monthly/yearly switch.
- Website: the feature overview shows Browser source & alerts, Voice presets, Transitions & studio mode, Add platforms while live and audio monitoring (EN/DE/IT).
- Website: anonymous visitor statistics with Cloudflare Web Analytics – no cookies, no user profiles, no cookie banner needed. The privacy policy (EN/DE) and the privacy statements on fabcomstudios.com say so.

### Fixed
- **Recordings now play in Windows Media Player** (and other strict players). MP4 recordings were missing the audio configuration ("Das Audio … ist im Format mp4a codiert" / black video at 00:00). FFmpeg, VLC and browsers played them, Windows Media Player refused. New recordings contain it; already recorded files keep the problem – open them with VLC or record them again.
- **Clips always have a picture:** a clip that started between two keyframes could be saved without video (only sound). Clips now start at the keyframe right before the moment (up to 2 s more lead-in).
- **Kick: the stream now arrives on the channel after *Fetch key*.** Kick hands out its ingest server without the RTMP application part (`/app`); FFmpeg then sent the stream to the wrong place and Kick dropped it. FabStream adds `/app` for Kick's (and Twitch's) Amazon IVS servers – also for destinations saved earlier.

## 1.11.0 – 2026-10-06

### Added
- **Browser Source – alerts, chat boxes, goal bars and any web overlay.** *Add Source → Browser Source*, paste the widget link (Streamlabs: Dashboard → Alert Box → *Widget URL*; StreamElements: your overlay link) – done. The page is shown with a transparent background and can be placed differently in 16:9 and 9:16 like every other source. Properties: address, size (with presets, also 1080×1920), frame rate, custom CSS, *Reload page*, and *Play the page's sound* so alert sounds reach the stream through desktop audio.
- **Efficient and safe:** every page runs in its own hidden, sandboxed browser without access to FabStream or your files. Only the parts of the page that change are transferred, so an alert box costs almost nothing between alerts. Pages cannot download files, open windows, use your camera or microphone, or navigate to local files. Widget links contain private tokens – FabStream never writes them into its logs.
- **Audio monitoring:** mixer ⋮ → *Monitoring* – *Monitor and output* (hear a source on your headphones while it streams) or *Monitor only* (hear it, but keep it out of the stream and the recording – e.g. a music cue or a co-host check). A green tag in the mixer shows it; one click turns it off. Choose the device under *Settings → Audio → Monitoring device*; if it is unplugged, FabStream falls back to the default output.
- Self-test: new checks "browser source renders" (transparent around the page content) and "canvas stays capturable with a browser source".

### Improved
- Long text inputs (e.g. widget links) are no longer cut off at 80 characters.

## 1.10.0 – 2026-10-06

First published version with everything prepared as 1.9.0 (1.9.0 was built but not released).

### Added
- **Add and remove platforms while you are live:** in *Outputs & Streaming → Stream destinations* every destination of a running format now has **Go live** (add it to the running stream) and **Remove** (stop streaming there). The other platforms are not interrupted – the new connection starts at the encoder's latest keyframe, so nobody watching on Twitch notices that you just added YouTube. Each platform shows its own state: *Live*, *Connecting…*, *Reconnecting…* or *Failed* (with **Retry**). Removing the last platform asks first and then ends the stream. Streamlabs has to stop the whole stream for this.
- After a dropped connection the stream reconnects with exactly the platforms that were live, including ones you added during the stream.
- **Automatic cloud sync (optional):** *Settings → Advanced → Cloud sync → Upload scenes and settings automatically*. When you are signed in, your changes are uploaded about 20 seconds after you make them (never stream keys). A newer copy from another PC is never overwritten – *Settings → Account* shows it and lets you load it or replace it, then automatic upload continues. Loading on another PC stays a manual step, because it replaces the setup there.

### Security
- Source settings changed in the editor are now checked against the same limits as an imported project (sizes, font sizes, text length, allowed values); settings that are not part of the source are refused.
- Stream keys still never appear in a log line; adding a platform while live hides its key in the logs as well.

### Website
- **Fabcom Studios website in Italian:** fabcomstudios.com/it/ – home, studio, engineering and contact in Italian, with the same automatic language choice and EN / DE / IT switch as the FabStream pages (legal texts stay English/German). Better search snippets: titles and descriptions name the company as a Swiss software company and stay within ~160 characters; hreflang, sitemap and structured data cover all three languages. Fixed: fabcomstudios.com/it/ showed the Italian FabStream home page instead of the company site.

### Admin tool (website)
- **Revenue page:** monthly recurring revenue (yearly plans as 1/12), projected yearly revenue, paying subscriptions per plan and billing period, and per month for the last 12 months the new subscriptions with the value of their first payment, refunds and cancellations. Manual and test-mode licenses are not counted.
- **CSV export** of the (filtered) license list for Excel – without license keys, protected against spreadsheet formulas, and written to the audit log.
- Licenses now remember whether they are billed monthly or yearly (shown on the license page).

## 1.8.0 – 2026-10-05

### Added
- **Website in Italian:** the FabStream pages (home, download, account, contact, checkout, thank-you page) are now also available in Italian at /it/. Visitors from Italy, San Marino and the Vatican – and visitors with an Italian browser in Switzerland, Germany, Austria and Liechtenstein – get Italian automatically; the language switch now offers EN / DE / IT. Legal texts stay in English and German (the German version is binding); Italian pages link to the English ones and say so.
- **Website: “Measured vs. Beta”:** a new section shows what has been measured (both formats at 1080p60, 0 dropped frames) and what is still being tested, with an invitation to become a tester.

### Improved
- **Website: honest performance claims.** Values without a published measurement are marked **Beta**: output above 1080p60 (1440p / 120 fps, 4K / 240 fps), more than 3 platforms per format, entry-level hardware (GTX 1650 class) with a game running and 60-minute sessions. Plan limits are now described as the highest *settings* a plan unlocks, not as a performance promise; the FAQ, download page and terms say so too.
- Website: tips for entry-level GPUs (start with 16:9 at 1080p60 and 9:16 at 720p or 30 fps).

### Fixed
- **Recording and streaming work again with image and video sources.** In 1.7.0 an image or video file in the scene made both buttons fail with "MediaRecorder: SecurityError … Canvas is not origin-clean" (followed by "FFmpeg stopped unexpectedly"). Files are now loaded with permission for the program canvas; as a safety net, a source that would still block capture is skipped (and logged) instead of breaking the output, and Record / Go Live check the canvas before starting an encoder and show one clear message.
- Self-test: new check "image source keeps recording possible" (an image file in the scene, both canvases must stay capturable).

## 1.7.1 – 2026-10-05

### Added
- **Voice presets with voice analysis:** mixer ⋮ → *Voice presets…* gives your microphone a complete studio chain in one click – **Cinematic Podcast**, Broadcast Radio, Clear Streamer, Gaming – Noisy Room, Warm & Intimate, Natural. *Analyse my voice* listens to 3 seconds of silence and you reading a sentence, then tunes level, noise gate, room echo reduction, EQ, de-esser, compressor and limiter to your voice, microphone and room (and tells you what it found, e.g. clipping, background noise or an echoing room). Tick *I use speakers* to cancel the speaker echo.
- New audio filters: **Voice EQ** (5-band parametric), **De-Esser**, **Room Echo Reduction** and **Warmth** (saturation).

### Improved
- **Back to FabStream after signing in:** when the browser shows "You are signed in" / "Your account is linked", it switches back to FabStream after 5 seconds (or at once with "Switch to FabStream now"; "Stay here" stops it) and closes the tab when you switch – where the browser allows a page to close its own tab, otherwise it says the tab can be closed.

### Security
- **Hardened FabStream.exe:** Electron fuses switched off (RunAsNode, NODE_OPTIONS, --inspect), so the signed app cannot be misused to run other code.
- **Saved keys are never lost by accident:** a locked or damaged key store is no longer overwritten (damaged files are kept as `secrets.json.corrupt-…`); the PC id used for licenses is only created anew when it is really missing.
- **Backups and cloud sync are safer:** network paths (`\\server\…`) in imported scenes are ignored, and when an imported destination points to a different server its saved stream key is deleted instead of being sent there.
- **A stream key pasted into the server URL** is detected (Twitch, Kick, YouTube, Facebook, TikTok, Trovo), moved to the key field and never stored in the settings file.
- **Licenses:** setting the system clock back no longer extends a subscription or the trial; offline keys with an invalid end date are refused; the update installer is checked again right before it starts.
- A second start of FabStream never closes an instance that is streaming or recording.

### Fixed
- Imported projects with odd values (e.g. huge text sizes or crafted names) can no longer crash FabStream; values are limited to what the editor allows.
- The hotkey recorder in Settings no longer keeps blocking the keyboard after switching tabs or closing the dialog.
- Stopping the replay buffer while a clip is being saved no longer breaks the clip.
- Two outputs started at the same moment can no longer bypass the plan limit or orphan an encoder.
- Clip library: files that disappear while listing no longer cause an error; a relative recording folder falls back to the default folder.

## 1.7.0 – 2026-10-05

First published version with everything listed under 1.6.0 (1.6.0 itself was not released).

### Improved
- Release build: packaging retries while Windows still holds the freshly tested FabStream.exe (no more "file in use" after the self-test).

## 1.6.0 – 2026-10-05

### Added
- **Sign in with Kick** (next to Twitch and TikTok, which are listed first) – and **connect Kick for streaming**: fetch your Kick stream key into a destination and set the stream title and category from Settings → Stream, like with Twitch.
- **Profile button** at the bottom right: your account, plan with **Upgrade**, Plan & license, Settings, report a bug, suggest an idea, sign in / out.

### Improved
- **Cleaner layout:** the title bar only shows FabStream. New scenes and sources are added with the `+` of the Scenes and Sources panels, **Record** and **Go Live** (all formats) are in the Outputs & Streaming panel.
- **Your plan decides what you can choose:** options of bigger plans (frame rate, resolution, replay length, more platforms per format, preview features) are shown with a 🔒 and the plan name but cannot be selected. When a trial ends or a plan changes, settings outside the plan are adjusted automatically – extra destinations are only switched off, never deleted.

### Removed
- **Steam sign-in.** Accounts that used Steam sign in with an e-mail code (or another linked sign-in) instead.

## 1.5.0 – 2026-10-05

### Added
- Website: home page links to the FabStream Product Hunt page (self-hosted badge – no third-party image or tracking).
- **FabStream account (optional).** Sign in with an e-mail code (no password) or with Twitch, Steam, TikTok, Discord or Google/YouTube – Settings → Account.
  - **Your plan on every PC:** plans bought with your account's e-mail address (or added with their key) work on any PC you sign in on – no license key to copy. Signing out frees the PC.
  - **Cloud sync:** upload scenes, sources and settings and load them on another PC. Stream keys never leave your PC.
  - **Twitch:** connect Twitch once, then fetch your stream key into a destination and change the stream title and category from Settings → Stream.
  - Manage everything in one place: linked sign-ins, signed-in devices, PCs per license, invoices & billing, delete account.
- **Report a bug / suggest an idea** right from Settings (bug and light-bulb buttons). Attach a log excerpt (stream keys and tokens are removed automatically), system info and a screenshot – only what you tick is sent.
- **Settings → Advanced:** turn the update check on start on or off, detailed (debug) logging, save and load a backup file of scenes + settings (never contains stream keys), and reset all settings to their defaults.
- **Scene transitions** on both formats at once: Cut, Fade, Fade to colour, Slide, Swipe, Wipe and **Stinger** (your own video, WebM with transparency or MP4, with sound and an adjustable switch point; optionally a separate 9:16 clip). Pick the default with the new transition button above the previews; any scene can have its own transition (scene menu → "Transition into this scene…"). Sound of video files fades along with the picture.
- **Studio mode:** prepare a scene in the preview while viewers keep seeing the live scene, then send it live with **Transition** (or **Cut**). Program and preview are shown for 16:9 and 9:16. Hotkeys for "send preview live" and "studio mode on/off" in Settings → Hotkeys. Leaving studio mode never changes what is live; the live scene cannot be deleted by accident.

### Improved
- Video files in scenes that are not live are now silent (before, their sound kept playing for a few seconds after switching away).

## 1.4.0 – 2026-10-05

### Added
- **Four plans: Free, Premium, Ultra and Max.**
  - Free: 16:9 + 9:16 at once, 1 platform per format, 1080p60, 2-minute replay buffer.
  - Premium ($4.99 / 4,99 € a month): 3 platforms per format, 1440p and 120 fps, 5-minute replay buffer, 1 PC.
  - Ultra ($9.99 / 9,99 €): 8 platforms per format, 4K and 240 fps, 10-minute replay buffer, 3 PCs.
  - Max ($19.99 / 19,99 €): everything in Ultra, 30-minute replay buffer, 5 PCs, early access to preview features (Auto Moments) and priority support.
  - Yearly plans: 2 months free.
- The upgrade dialog shows all plans side by side and recommends the plan a feature needs; settings mark options with the plan they need ("· Ultra").
- The 7-day trial now unlocks everything (Max).
- Website: four plan cards with prices in US$ (English) and € (German).

### Fixed
- **Website address:** the website, your account and license checks now run on https://fabstream.fabcom-dev.workers.dev (1.3.1 pointed to an address that is not in use). Please update.

## 1.3.1 – 2026-10-05

### Fixed
- **New website address:** FabStream now uses https://fabstream.fabcom.workers.dev for Premium, your account and license checks. Please update – version 1.3.0 still points to the old address.
- **Recordings and clips are never overwritten:** two recordings or clips started in the same second get separate files (`_2`, `_3` …).
- **Update download:** a full disk, missing write access or a dropped connection now ends the download at once with a clear message (before, it could hang).
- **Long replay sessions:** the replay buffer's segment list stays small however long you stream, and segments a clip is being cut from are kept until the clip is done.
- **Security:** FabStream only loads image and video files you chose yourself (network shares only when picked explicitly).
- **License server:** a PC limit can no longer be exceeded by activating several PCs at the same moment; late or repeated payment notifications can no longer switch a subscription back to an older state; only FabStream purchases (in the right test/live mode) create license keys; a license e-mail that could not be sent is sent again automatically; checkout attempts are rate limited.

### Improved
- **Website:** English by default, German for visitors from Germany, Austria, Switzerland and Liechtenstein; the EN/DE switch remembers your choice.
- **GitHub page:** what's new, supported platforms, keyboard shortcuts, more FAQ and a German summary.
- **Builds:** every release is compiled fresh from the source, runs the app and license-server tests and the self-test, and uses a locked FFmpeg build; each package records exactly what it contains (`build-info.json`).

## 1.3.0 – 2026-10-05

### Added
- **One encoder per format:** recording, every stream destination and the replay buffer of a format now share ONE encoder (before: one per output). Streaming + recording + replay buffer in 16:9 and 9:16 needs 2 encoder sessions instead of 6 – much less GPU load, no NVENC session limit problems.
- **Application audio:** Audio Mixer → Add Audio → *Application Audio* records a single program – e.g. Discord, Spotify or a game – as its own channel with volume, mute and filters. FabStream lists the programs that are playing sound; programs that are not running yet are picked up automatically when they start (and again after a restart).
- **Desktop Audio → Leave out application:** keep one program (e.g. Discord) out of the desktop mix – so it is not recorded at all, or only through its own fader. Adding an application channel does this automatically, so nothing is recorded twice.
- **Auto Moments (preview):** while the replay buffer runs, a loud reaction on your microphone or a loud moment in the game sound becomes a suggestion card with "Save clip" (or is saved automatically, max. 12 per hour). Settings → Replay & Clips → Auto Moments. Only levels are analysed, nothing leaves your PC; every suggestion is on the session timeline.
- **Keyboard control:** Esc = back (closes dialogs and menus, deselects), Enter = accept (OK / Save / Delete), Delete removes the clicked scene or source (with confirmation), arrows switch scenes / layers or nudge the source, F2 rename, Ctrl+N new scene, Ctrl+1…9 switch scene, Ctrl+Shift+D duplicate, Ctrl+, settings, arrow keys in menus. **F1** shows all shortcuts.
- **More video options:** output resolutions from 640×360 up to **4K** (3840×2160 / 2160×3840) and frame rates up to **240 fps**. FabStream now renders each format at exactly the output resolution – 1440p/4K are real, not upscaled, and smaller outputs cost less GPU.
- **BENCHMARK.cmd:** measures FabStream on your PC (stream + recording + replay in both formats at 1080p60) and writes a short report.
- **Output health** in the Outputs panel: warns when the encoder is overloaded, frames are dropped, the upload or the disk is too slow, or a destination reconnects.

### Improved
- **Multistream:** if one platform drops, only that destination reconnects – the others keep streaming without interruption.
- **Encoder supervision:** an encoder that crashes is restarted automatically (max. 3 times in 5 minutes); recordings continue in a second file (`…_part2`), streams re-publish.
- Recordings started while streaming begin immediately (from the last keyframe) instead of starting a second encoder.
- **Plans updated:** Free covers dual output, recording, replay clips (last 2 min), application audio and everything else up to 1080p at 60 fps. Premium adds multistream, 1440p/4K, up to 240 fps and a 10-minute replay buffer. Premium options are marked in the settings; starting them on Free opens the upgrade dialog.

### Fixed
- Application audio finds the right program after restarts (process ids are re-used by Windows; Discord's parent process exits) and only in your own Windows session; a game started as administrator is re-attached after it restarts.
- Desktop audio: unplugging the only headset shows "reconnecting" instead of staying "live", without filling the log every second.
- FabStream no longer shows up as an audio application (Windows volume mixer, Application Audio list): its mixer runs without opening a playback device.

## 1.2.0 – 2026-10-04

### Added
- **Replay buffer & instant clips:** keeps the last 30 s – 10 min of both formats; **Save clip** (button or Ctrl+Shift+C) writes the moment as MP4 – 16:9 and 9:16 at once, instantly, without re-encoding. Configurable seconds before/after.
- **Mark moment** (Ctrl+Shift+M) and a session timeline per stream (events and moments as JSONL next to your recordings).
- **Clip library:** play, show in folder, delete to the recycle bin; Highlight Score per clip.
- Settings → Replay & Clips; Diagnostics → Features (feature flags) and Advanced diagnostics.
- Settings → Audio → **Desktop audio capture**: Automatic (recommended) / all apps except FabStream / default playback device / legacy.

### Improved
- Buttons in the Outputs panel no longer miss clicks while live statistics update.

### Fixed
- **Desktop audio with headsets and when switching the sound output:** desktop audio is now captured by FabStream's own Windows audio helper. It works with devices Chromium could not open (Logitech G HUB 7.1, DualSense …), keeps running when you switch speakers ↔ headset, re-connects after a device is unplugged, and no longer records FabStream's own monitoring sound. The old capture path remains as an automatic fallback and now re-connects after a device switch too.

### Security
- The app UI can no longer open files directly (folders only); clips open through a checked path.

## 1.1.0 – 2026-10-04

### Added
- Settings → General: confirm before stopping, record automatically when going live, keep the PC awake while live, start with Windows.
- Settings → Hotkeys: start/stop streaming and recording, next/previous scene, mute microphones/desktop audio – in-app or global (also while gaming), with conflict messages.
- Settings → Advanced: process priority for FabStream and its encoders.
- Encoder: CBR/VBR rate control and H.264 profile. Stream: reconnect on/off, attempts and delay. Recording: file name prefix.
- In-app updates: FabStream checks GitHub on every start; "Update & restart" downloads the new version, verifies the Ed25519-signed checksum and the SHA-256, installs it and restarts FabStream.
- Release notes with SHA-256, signed `SHA256SUMS.txt`, SECURITY.md.

### Improved
- Desktop audio: clear message when Windows cannot capture the playback device; audio sources restart automatically when devices change.

### Known issues
- The installer is not code-signed yet: Windows SmartScreen asks for confirmation, and Windows 11 Smart App Control blocks it. The Microsoft Store version is signed by Microsoft.
- Desktop audio is captured from the Windows default playback device; some devices (e.g. game-controller headsets) cannot be captured – choose another output device.
- Multistream sends each destination from your PC, so it needs upload bandwidth for every destination.

## 1.0.0 – 2026-10-04

### Added
- Dual-format studio: one project, two independently designed canvases (16:9 and 9:16), streamed and recorded at the same time.
- Free plan: dual output (one platform per format), recording of both formats, all filters, no watermark, no time limit.
- Premium (optional subscription, 7-day trial in the app): multistream to up to 8 RTMP destinations per format, 3 PCs.
- Hardware encoding (NVIDIA NVENC, AMD AMF, Intel Quick Sync) with automatic x264 fallback.
- Safe-zone overlays for TikTok, Shorts and Reels; GPU video filters; audio mixer with filters.
- Update notice when a new version is published (no automatic download or installation).

### Known issues
- The installer is not code-signed yet: Windows SmartScreen asks for confirmation, and Windows 11 Smart App Control blocks it. The Microsoft Store version is signed by Microsoft.
- Multistream sends each destination from your PC, so it needs upload bandwidth for every destination.
