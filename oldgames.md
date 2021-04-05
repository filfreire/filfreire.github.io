---
layout: page
title: Personal notes on running old games
meta_description: "Personal notes on running old games"
permalink: /oldgames/
---

This is a personal page where I take note of steps I took in order to be able to play some older DOS/Win95 games so I won't forget about them.

- **Disney's Timon & Pumbaa's Jungle Games** - [Download link](https://www.myabandonware.com/game/disney-s-timon-pumbaa-s-jungle-games-3j3) - On the Downloads section, use the FIX installer. It should install the Game + a standalone DOSbox and should work on Windows 10 x64.

- **Bionicle** (Nestle promotional cd game) - [Download link](https://biomediaproject.com/bmp/promo-cds/nestle/) - Setup and game should work ok on Windows 10 x64, if there are issues, try to run in compatibility mode.

- **Disney's Arcade Frenzy** - [Download link](https://collectionchamber.blogspot.com/p/disneys-arcade-frenzy.html) - use the MEGA download link on the page, and download both files there (there `.exe` and the `.D01`), run the installation, and then start the game. It should open up a Windows 95 "vm" - just click on the game icon on the desktop of that VM.

- **Disney's Animated Storybook: 101 Dalmatians** - [Download link](https://collectionchamber.blogspot.com/p/disneys-animated-storybook-101.html) - use the MEGA download link on the page, and download both files there (there `.exe` and the `.D01`), run the installation, and then start the game.

- **The Land Before Time Activity Center** - [Download link](https://archive.org/details/thelandbeforetimeactivitycentercdrom) - on the download options of the page, download the ISO file (or get it with the torrent), rename to `LBT.iso` and then, copy the iso to the `CD` folder of the ***Disney's Arcade Frenzy*** installation, and edit the final `imgmount` command of the  `dosbox.conf` file to look like:
```
imgmount d: "CD\LBT.iso" -t iso -fs iso -ide 2m
```
Then run `Run.exe` file on the the ***Disney's Arcade Frenzy*** installation, and try to install the game on that windows 95 machine (go to windows explorer and you should see the CD there mounted). After installing it should add shortcuts to the start menu for the game, and you should be able to run those and boot up the game.


> Last updated: 5 April 2021