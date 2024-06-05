---
Label: GTA 5 [Epic Games]
---

As of 06/06/2024, I recommend using [Heroic](https://github.com/Heroic-Games-Launcher/HeroicGamesLauncher) to install the game, since a bug with Lutris causes the Epic Games Store to blank out.

After downloading the game & installing the launcher, you might encounter a network error 134. According to [this reddit post](https://www.reddit.com/r/SteamDeck/comments/1awzm24/gta_v_error_134_heroic/), set this file as the alternative .exe, and make sure to place it in the game's root folder:

``` fix.bat
start /B "null" "C:\Program Files\Rockstar Games\Launcher\LauncherPatcher.exe"

ping -n 20 localhost > nul

./PlayGTAV.exe %*
```