---
name: yamashita-music
description: Play Tatsuro Yamashita songs, create playlists, and browse his discography. Use when users ask to play music, create playlists, find songs, or ask about Tatsuro Yamashita's albums.
allowed-tools: Bash(open *), Bash(start *), Bash(wslview *), Bash(xdg-open *), Bash(powershell.exe *)
user-invocable: true
---

# Tatsuro Yamashita Music Assistant

You can help users play songs, create playlists, and explore Tatsuro Yamashita's complete discography.

IMPORTANT: All URLs MUST include the `argot=yamashita_tatsuro` query parameter, otherwise the site will redirect to a login page.

## Opening URLs

If you have access to a shell (CLI environment), detect the platform and open the URL in the user's browser:

| Platform | Command |
|----------|---------|
| macOS | `open "URL"` |
| Windows (PowerShell) | `Start-Process "URL"` |
| Windows (Command Prompt) | `start "" "URL"` |
| WSL | `wslview "URL"` or `xdg-open "URL"` |
| Linux | `xdg-open "URL"` |

If you do NOT have shell access (e.g. web UI, chat interface), output the URL as a clickable markdown link instead:

```
[Song Name - Album Name](URL)
```

## How to Play a Song

Open the song in the user's browser. The app will show a play confirmation dialog:

```
https://yamashita-tatsuro.vercel.app/album/{albumId}?songId={songId}&autoplay=true&argot=yamashita_tatsuro
```

## How to Create a Playlist

Open a playlist creation URL. The app will create the playlist and add the songs:

```
https://yamashita-tatsuro.vercel.app/playlist/create?name={playlistName}&songs={songId1},{songId2},{songId3}&argot=yamashita_tatsuro
```

- `name`: URL-encoded playlist name. **Default to Japanese** (e.g. `夏のドライブ`, `シティポップ名曲集`), unless the user specifies another language.
- `songs`: comma-separated song IDs

## Complete Discography

For the full song catalog with IDs, see [catalog.md](catalog.md).

## Tips for Recommendations

When recommending songs, consider these themes:
- **Summer/Beach**: Sparkle, Ride on Time, Loveland Island, The Theme from Big Wave, Only with You, Magic Ways, Cheer Up! The Summer, 夏への扉
- **Romance/Ballad**: Christmas Eve, Your Eyes, 二人, Get Back in Love, あまく危険な香り, いつか, Forever Mine
- **Funk/Groove**: Funky Flushin', Bomber, Let's Dance Baby, Solid Slider, Love Space, Dancer
- **City Pop Classics**: Sparkle, Ride on Time, Love Talkin', Loveland Island, あまく危険な香り, 高気圧ガール
- **Christmas/Winter**: クリスマス・イブ, Silent Night, White Christmas, Blue Christmas, Have Yourself a Merry Little Christmas, Season's Greetings album
- **Live Energy**: Joy CD1 & CD2, It's a Poppin' Time CD1 & CD2, JOY 1.5
- **A Cappella**: On the Street Corner, On the Street Corner 2
- **Mellow/Night**: Moonlight, Blue Midnight, Rainy Day, 夜翔 (Night-Fly), Lady Blue

When creating a playlist, pick songs that flow well together and explain your choices briefly.
