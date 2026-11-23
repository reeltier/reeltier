# ReelTier: 5-minute guide

ReelTier organizes your video collection. You give each video a tier, it moves itself to the right folder, gets renamed with its data (performer, studio, date), and you get statistics about what you like. Everything runs on your PC.

## 1. Install and pick folders

1. Run `ReelTier-Setup.exe`. It does not need administrator rights.
2. Your browser opens `http://localhost:8770/configurar`. Choose:
   - **Downloads:** where new videos land.
   - **Library:** where rated videos will live.
   - **Folder layout:** how tiers (q0 to q3) are split into folders, and whether file names may be changed.
3. Done. The app lives at `http://localhost:8770/app`.

## 2. Day to day

- **Today:** what is worth doing now (duplicates, unrated videos, matches to check) and news from your favorite performers.
- **Review → Rate:** the video plays large. Rate it from 1 to 10, IMDb style: keys `1` to `9`, and `1` `0` in a row for a 10. From 6 to 10 the video stays, each rating in its folder (9 and 10 in the top one); 1 to 5 sends it to the trash with that rating. When playback stops, the file moves.
- **Review → Matches:** ReelTier looked the scene up in ThePornDB, StashDB and FansDB. Press `S` if it is that scene, `N` if not. Accepting renames the file with the right data.
- **Review → Unresolved:** what nobody has confirmed yet, with the reason in plain words and bulk buttons.
- **Library:** everything, with filters, hover previews and multi-select (Ctrl+click).
- **Statistics:** click any bar to filter everything, Power BI style. "Your taste over time" compares periods and exports to CSV.
- **Undo:** `Ctrl Z` or the "Undo last" button reverts the last move.
- `?` shows every shortcut; `Ctrl K` opens quick search.

## 3. From your headset (Meta Quest and similar)

With the PC and the headset on the same Wi-Fi:

- **HereSphere:** add the library `http://<your PC's IP>:8770/heresphere`. Each half star is one point of the rating: 5 stars = 10, 4.5 = 9, 4 = 8, and 2.5 or less goes to the trash with that rating. Timeline markers and `Lista:Name` tags sync with the app.
- **DeoVR:** same address with `/deovr`.
- **Headset browser:** `http://<your PC's IP>:8770/` is the finger-friendly rating page.

Your PC's IP is shown at the bottom left of the app ("Rate from the Quest").

## 4. Automatic subtitles

ReelTier listens to the audio of what you keep (q0 and q1 by default) and saves subtitles next to each video, in the original language and translated (`video.en.srt`, `video.es.srt`). It does this on its own while you are not watching anything. Turn them on and pick the language in the player.

## 5. Several people and security

In **Settings → Access**, set a PIN or create users with three roles: everything, rate only, or watch only. Without a PIN, any device on your Wi-Fi gets in as the owner. The app only answers your home network and rejects requests coming from other web pages.

## FAQ

**Does it delete anything?** No. The trash is a folder (`_papelera`) that you empty yourself.

**Does it upload my collection anywhere?** No. Only the title, performers, studio or the file's fingerprint (a code, not the video) leave your PC, to identify scenes. Full details in Help (`?`) → Privacy.

**A rename went wrong. Now what?** In the video's details, "Edit name". For a whole batch, `python renombrar.py --deshacer`.

**Can I bring in what I had in Stash?** Yes: `Ctrl K` → "Import from Stash" reads its database without changing it.

**Does it work with Plex, Jellyfin or Kodi?** Yes: `Ctrl K` → "Export .nfo files" writes each video's details next to the file, in the format those apps read.

**The power went out in the middle of a copy. Did I lose the video?** No: the original is deleted only after the copy is written to disk and verified.
