<p align="center">
  <img src="./images/web_header.gif" alt="MissionForce: CyberStorm Logo">
</p>
A fan-driven historical archive dedicated to MissionForce: CyberStorm — Sierra’s dark, tactical science-fiction wargame that combined brutal turn-based combat, persistent pilots, and corporate warfare into one of the most unforgiving strategy experiences of the 1990s.

# Motivation
Despite its age, *MissionForce: CyberStorm* is not truly dead. Player uploads, scattered discussions, and surviving archives prove there is still a pulse beneath the surface. More importantly, the game remains fully playable on modern systems and is legally available through [GOG.com](https://www.gog.com/en/game/missionforce_cyberstorm), creating a rare opportunity to introduce a new generation of players to one of Sierra’s most overlooked strategy titles.

The challenge is visibility. CyberStorm suffers from decades of underrepresentation in gaming media, disappearing fan sites, and mechanics that were never properly explained to newcomers. For many players, the barrier is not the game itself — it is simply discovering how deep and rewarding it actually is.

Other classic communities have already demonstrated what is possible when passionate fans refuse to let a game disappear. Projects like [OpenTTD](https://www.openttd.org/), [OpenXcom](https://openxcom.org/), and [OpenRCT2](https://openrct2.io/) transformed aging titles into thriving modern communities through preservation, documentation, multiplayer support, and community-driven development.

There is no reason *MissionForce: CyberStorm* should remain without a community presence. The foundation still exists — the game is obtainable, functional, and mechanically unique even by modern standards. What is missing is a centralized effort to preserve knowledge, document its systems, archive its history, and make entry into the game approachable for new players.

# Publications
## [Prima Strategy Guide](./publications/Prima%20Strategy%20Guide.pdf)
John Sauer wrote an official strategy guide for MissionForce: CyberStorm under the Prima Publishing label. Produced with direct support from Dynamix, the guide provides extensive gameplay information, mechanics explanations, and strategic insight that were largely absent from the retail release.

Given the depth and importance of its content, the guide arguably should have served as the in-box manual for players.

## [Quick Reference Card](./publications/Quick%20Reference%20Card.pdf)
The game came with a quick reference Card which seemingly contains unique information, such as keyboard hotkeys.

It also informs the player of the maximum commander rank achievable within a star system. Not knowing this can cause players to grind unnecessarily (Missing Promotion Points). The card also includes a cost-to-performance comparison chart for purchasable derms (Missing learn rates). While this information exists in-game, it is only shown one item at a time, making direct comparison difficult.

A major highlight is the keyboard hotkeys. The game can become grind-heavy, so these shortcuts are an important quality-of-life tool:

- Crouch/Stand: `K`  
- Move shields forward: `-`  
- Inject derm with Jackup: `[`  
- Show/Hide terrain: `0` & `9`  
- Next/Previous HERC: `<` & `>`  
- End turn: `Ctrl + E`

Staying on the Fire Control Panel as much as possible significantly speeds up overall gameplay.

However, gameplay patterns show that players often neglect the Crouch and Jackup mechanics, as they are usually not worth the time investment in most situations. This leads to them being forgotten in moments where they are most needed.

My typical workflow is to spam `-[>` at the start of each battle, then ending each turn with `K>` ending with `Ctrl + E`.

## InterAction Magazine
*InterAction* was a dedicated promotional magazine published by Sierra On-Line starting in June 1991. Archival pages were sourced from [Retromags](https://www.retromags.com/files/category/206-interaction/).

### [Issue 27 (Summer 1996)](./publications/InterAction%20Issue%2027%20(Summer%201996).pdf)
- Pages 28–31 showcase the game using prerelease assets.
- Advertises the inclusion of two copies in each box to encourage online play.

### [Issue 28 (Fall 1996)](./publications/InterAction%20Issue%2028%20(Fall%201996).pdf)
- Page 7 sells a swag T-shirt featuring *MissionForce: CyberStorm* branding.
- Page 13 lists *CyberStorm* as #4 in the Top 10 Entertainment rankings.
- Pages 68–71 contain a multi-page article praising the multiplayer experience, although gameplay imagery is sparse.

### [Issue 29 (Holiday 1996)](./publications/InterAction%20Issue%2029%20(Holiday%201996).pdf)
- Page 10 lists *CyberStorm* as #7 in the Top 10 Entertainment rankings.
- Pages 96–97 promote multiplayer features, the [www.sierra.com/cyberstorm](https://web.archive.org/web/19970214174036/http://www1.sierra.com/games/cyberstorm/index.html) website, and the message board.
- References daily tournaments with approximately 200 participants in the Red Max's 1996 *Storm Watch Challenge*. While not hosted directly by Sierra, the company provided prizes and official rules.
- The utility *Madaxe's HercView* is endorsed and made available for download.
- A bundle containing 96 HERC save file was also distributed.
- Cheat codes were published through the [goodies webpage](https://web.archive.org/web/19970214174036/http://www1.sierra.com/games/cyberstorm/index.html), which appears to have been the primary source for updates, with indications that new codes may have been added monthly.

### [Issue 30 (Spring 1997)](./publications/InterAction%20Issue%2030%20(Spring%201997).pdf)
- Page 87 announces *CyberStorm 2* with the casual mention:

> "If you are one of the zillion people who demanded more of MissionForce: CyberStorm, then the creative team of designers at Dynamix is putting together a game you're gonna love."

- *CyberStorm* was absent from the Top 20 section on page 96.

## [Installation Guide](./publications/Installation%20Guide.pdf)
The installation guide is nearly useless and represents the absolute bare minimum of acceptable documentation.

Given the complexity of the game’s mechanics, the absence of a proper physical manual was a disappointment frequently voiced by players. It is difficult to imagine that many users did not mistake the installation guide for the nonexistent game manual itself. The 1.2 patch notes even acknowledge complaints regarding the lack of a printed manual.

The situation was likely made worse by how comically thin the installation guide appeared. Although it does reference the in-game/on-disk manual, the mention is extremely easy to miss. It also briefly hints that some sounds were sourced from the "Sound Ideas® sound effects library."

# Downloads
## Madaxe's HercView 1.1
James Parker “Madaxe” created a utility called HercView that enabled players to view and print `.hrc` files outside of CyberStorm ([example](./downloads/HercView/Example.pdf)). The tool received direct support from Sierra On-Line, being hosted on Sierra’s “Extra Goodies” page and later referenced in InterAction Issue #29.

The version provided requires [installation](./downloads/HercView/Installer.zip), while a [portable](./downloads/HercView/Portable.zip) edition has been created for preservation purposes.

The Herc Base Alpha website documents the `.hrc` [file specification](https://web.archive.org/web/19991007062427/http://www.uncg.edu/%7Ejsrobard/CS_Hacking.htm#edit_cbs), making it straightforward to develop a modern implementation.

## HERCs R Us
Sierra produced a collection of [89 custom .hrc](./downloads/89_Hercs.zip) files as a special release for Christmas 1996. Issue 29 of InterAction states that the files were created by Dynamix QA technician Matthew Vincent.

Without additional tools, `.hrc` files are difficult to effectively use or evaluate in single-player. If a player's technology level exceeds the HERC design, the imported HERC becomes underpowered. Conversely, if the `.hrc` file requires a higher tech level than the player has achieved, the HERC cannot be imported at all.

## [v1.1 Patch](./downloads/v1.1%20Patch.zip)
Patch v1.1 was a major overhaul for the game, introducing Hotseat multiplayer and Play-by-Email multiplayer support. It also rebalanced gameplay, particularly around the first Elite mission, added additional cheats and openly documented them within the game files, and introduced the Opportunity Fire mechanic, allowing both players and AI units to take reactive “overwatch” shots.

With the sheer number of improvements and gameplay refinements, v1.1 stands as the quintessential way to experience the game. No other updates or patches were officaly released by Sierra / Dynamix.

## [v1.2 Homebrew Patch](./downloads/v1.2%20Homebrew%20Patch.zip)
The fans `Crow!`, `Seraphim`, `borg_down`, `siopaomanX` on [The Junkyard forums](https://web.archive.org/web/20121128141129/http://forums.the-junkyard.net/showthread.php/8480-Cyberstorm-Single-Player-V1.2-(Now-it-actually-works!)) created a homebrew patch for the single-player campaign in 2007. The patch primarily focuses on increasing the game’s difficulty by modifying the equipment loadouts used by Cybrid enemies.

Special thanks for the dedication and expertise required to create such a patch. Rebalancing a complex strategy game at this level demands a deep understanding of its mechanics, enemy scaling, and overall campaign flow (Dynamix has 14 Quality Assurance Analysts listed in the credits). Truly a legend!
