<p align="center">
  <img src="./images/web_header.gif" alt="MissionForce: CyberStorm Logo">
</p>
A fan-driven historical archive dedicated to MissionForce: CyberStorm — Sierra’s dark, tactical science-fiction wargame that combined brutal turn-based combat, persistent pilots, and corporate warfare into one of the most unforgiving strategy experiences of the 1990s.

# Motivation
Despite its age, *MissionForce: CyberStorm* is not truly dead. Player uploads, scattered discussions, and surviving archives prove there is still a pulse beneath the surface. More importantly, the game remains fully playable on modern systems and is legally available through [GOG.com](https://www.gog.com/en/game/missionforce_cyberstorm), creating a rare opportunity to introduce a new generation of players to one of Sierra’s most overlooked strategy titles.

The challenge is visibility. CyberStorm suffers from decades of underrepresentation in gaming media, disappearing fan sites, and mechanics that were never properly explained to newcomers. For many players, the barrier is not the game itself — it is simply discovering how deep and rewarding it actually is.

Other classic communities have already demonstrated what is possible when passionate fans refuse to let a game disappear. Projects like [OpenTTD](https://www.openttd.org/), [OpenXcom](https://openxcom.org/), and [OpenRCT2](https://openrct2.io/) transformed aging titles into thriving modern communities through preservation, documentation, multiplayer support, and community-driven development.

There is no reason *MissionForce: CyberStorm* should remain without a community presence. The foundation still exists — the game is obtainable, functional, and mechanically unique even by modern standards. What is missing is a centralized effort to preserve knowledge, document its systems, archive its history, and make entry into the game approachable for new players.

# Ways to play
1. **Digital Release**  
   [GOG.com](https://www.gog.com/en/game/missionforce_cyberstorm) sells the game for approximately **$5.99 USD**.  
   This release includes the **v1.1 patch** and runs out of the box on modern systems, aside from missing links to the external Windows help and manual files.

2. **Original CD Release**  
   [eBay](https://www.ebay.com) frequently has loose CD copies available for around **$10.00 USD**, while complete boxed copies typically sell for around **$60.00 USD**.  
   Physical releases usually require manual intervention to install updates and run properly on modern operating systems.

3. **Preservation Copy**  
   [Archive.org](https://archive.org/details/missionforce-cyberstorm) hosts preserved `.iso` image of the game.  
   This versions also require manual intervention to install patches and configure compatibility on modern systems.


# Preservation status
To properly preserve the game and ensure compatibility with future devices and software, the assets contained within the game should be extracted or otherwise separated in a structured way. Ideally, this process should be reversible, allowing improved assets—such as higher-quality audio files—to be reinserted into the game later. There also appears to be overlap between multiple Dynamix projects, suggesting that there may be useful cross-project insights or shared preservation techniques applicable to games from that era.

## Music
Progress: 🟩🟩🟩🟩🟩⬜⬜⬜⬜⬜ 50%

Progress so far: Loose `.ogg` files.

Next step: Extract the redbook audio direct from disk (Cannot be done from GOG version).

## SFX
Progress: 🟩⬜⬜⬜⬜⬜⬜⬜⬜⬜ 10%

Progress so far: The `.rbx` have been examined / dumped produceing a collection of `.wax` files. 

Next step: The `.wax` files need slight tweaking to convert into modern `.wav` files. (There already is a [decoder](https://github.com/juanitogan/rbxit/blob/master/tools/wax2wav.py))

## Graphics
Progress: ⬜⬜⬜⬜⬜⬜⬜⬜⬜⬜ 0%

Progress so far: The `.rbx` have been examined / dumped produceing a collection of files however no art files imediatly standout.

Next step: Use Ghidra at the `.exe` to hint what file contains graphics then step the progress into a GDI display call.

## Fonts
Progress: 🟩⬜⬜⬜⬜⬜⬜⬜⬜⬜ 10%

Progress so far: Six files have been identified as likely canidates (FONTX.FNX)

Next step: Shim / dll injection the GDI call [CreateFontA](https://learn.microsoft.com/en-us/windows/win32/api/wingdi/nf-wingdi-createfonta?utm_source=chatgpt.com) to see how it is being pulled in. 

## Documents (Active Focus)
Progress: 🟩🟩🟩🟩🟩🟩🟩⬜⬜⬜ 70% 

Progress so far: v1.1 documents, scan from Prima gtrategy guide, InterAction issues, boxed game includes, relevant InterAction issues.

Next step: The game relied on a digital manual to explain mechanics to users. The game calls `MVIEWER2.exe` then loads the english manual `METALSTO.MVB` however this application does not work on modern systems. `METALSTO.MVB` has been extracted into `.rtf` files along with the imbedded images. After the extraction the `.rtf` documents have been converted into modern `.html` files for viewing. Reconstructing the page linking is nearly complete.

## 3D Assets
Progress: ⬜⬜⬜⬜⬜⬜⬜⬜⬜⬜ 0%

Progress so far: Unkown

Next step: Marketing materials state that high-quality 3D models were used to create game assets, but it is unclear whether any of those models were actually included in the final game. The 3D models may have been used for elements such as targeting obscurion and the hercbay wireframe. However, it’s also possible the assets were rendered down into a sprite sheet, with no actual 3D models present in the finished product. Between the start menu animations, the 360 hercbay wireframes and just the vertix count of 1996 a reconstruction of 8 Unitech HERCS apears easy with the 8 cybrid HERCS trickier to reconstruct without the 360 hercbay wireframes. Assets such as the carrier, buildings, bioderm heads, and turrets are suspected to be 3D in source only.

## Videos
Progress: 🟩🟩⬜⬜⬜⬜⬜⬜⬜⬜ ?%

Progress so far: Three `.avi` documents have been preserved pulled directly from the loose game install files.

Next step: Video files such as Bioderm deaths can easily be recorded however a better preservation would be to extract the bits from the `.rbx` files sources. Some videos are full screen such as the intro video and credits while others are imbedded into a larger composit such as Bioderm faces within the Medvat.

## Debugger
Cyberstorm pauses code execution while it doesn't have window focus complicateing the effectiveness of attaching x32dbg. If this pause mechanic can be disabled useing Ghidra then it would assist stepping through the code execution. Instruction stepping should pinpoint the RNG issue the game has when generateing new solar system missions. (It is expected that modern computers run too fast so each mission is generated useing the same seed ms causing the duplications)

# Publications
## Prima Strategy Guide
John Sauer wrote an [official strategy guide](./publications/Prima%20Strategy%20Guide.pdf) for MissionForce: CyberStorm under the Prima Publishing label. Produced with direct support from Dynamix, the guide provides extensive gameplay information, mechanics explanations, and strategic insight that were largely absent from the retail release.

Given the depth and importance of its content, the guide arguably should have served as the in-box manual for players.

## Quick Reference Card
The game came with a [quick reference Card](./publications/Quick%20Reference%20Card.pdf) which seemingly contains unique information, such as keyboard hotkeys.

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

### Issue 27 (Summer 1996) [PDF](./publications/InterAction%20Issue%2027%20(Summer%201996).pdf)
- Pages 28–31 showcase the game using prerelease assets.
- Advertises the inclusion of two copies in each box to encourage online play.

### Issue 28 (Fall 1996) [PDF](./publications/InterAction%20Issue%2028%20(Fall%201996).pdf)
- Page 7 sells a swag T-shirt featuring *MissionForce: CyberStorm* branding.
- Page 13 lists *CyberStorm* as #4 in the Top 10 Entertainment rankings.
- Pages 68–71 contain a multi-page article praising the multiplayer experience, although gameplay imagery is sparse.

### Issue 29 (Holiday 1996) [PDF](./publications/InterAction%20Issue%2029%20(Holiday%201996).pdf)
- Page 10 lists *CyberStorm* as #7 in the Top 10 Entertainment rankings.
- Pages 96–97 promote multiplayer features, the [www.sierra.com/cyberstorm](https://web.archive.org/web/19970214174036/http://www1.sierra.com/games/cyberstorm/index.html) website, and the message board.
- References daily tournaments with approximately 200 participants in the Red Max's 1996 *Storm Watch Challenge*. While not hosted directly by Sierra, the company provided prizes and official rules.
- The utility *Madaxe's HercView* is endorsed and made available for download.
- A bundle containing 96 HERC save file was also distributed.
- Cheat codes were published through the [goodies webpage](https://web.archive.org/web/19970214174036/http://www1.sierra.com/games/cyberstorm/index.html), which appears to have been the primary source for updates, with indications that new codes may have been added monthly.

### Issue 30 (Spring 1997) [PDF](./publications/InterAction%20Issue%2030%20(Spring%201997).pdf)
- Page 87 announces *CyberStorm 2* with the casual mention:

> "If you are one of the zillion people who demanded more of MissionForce: CyberStorm, then the creative team of designers at Dynamix is putting together a game you're gonna love."

- *CyberStorm* was absent from the Top 20 section on page 96.

## Installation Guide
The [installation guide](./publications/Installation%20Guide.pdf) is nearly useless and represents the absolute bare minimum of acceptable documentation on how to install and troubleshoot. 

Given the complexity of the game’s mechanics, the absence of a proper physical manual was a disappointment [voiced by players](https://groups.google.com/g/comp.sys.ibm.pc.games.strategic/c/KwuVW36djSw/m/vDhxq69hIDsJ). It is difficult to imagine that many users did not mistake the installation guide for the nonexistent game manual itself. 

> "However, the choice to not have a paper  manual was not one that many were, shall we say, fond of." In addition to the lack of heft in the box, many missed explicitly detailed statistics for the weapons. Some wanted more things to be able to read off-line. Others had trouble printing sections of the manual on their printer."
>
> — PATCH.TXT document (post install from v1.1)

The situation was likely made worse by how comically thin the installation guide appeared. Although it does reference the in-game/on-disk manual, the mention is extremely easy to miss. It also briefly hints that some sounds were sourced from the "Sound Ideas® sound effects library."

# Downloads
## Madaxe's HercView 1.1
James Parker “Madaxe” created a utility called HercView that enabled players to view and print `.hrc` files outside of CyberStorm ([example](./downloads/HercView/Example.pdf)). The tool received direct support from Sierra On-Line, being hosted on Sierra’s “Extra Goodies” page and later referenced in InterAction Issue #29.

The version provided requires [installation](./downloads/HercView/Installer.zip), while a [portable](./downloads/HercView/Portable.zip) edition has been created for preservation purposes.

The Herc Base Alpha website documents the `.hrc` [file specification](https://web.archive.org/web/19991007062427/http://www.uncg.edu/%7Ejsrobard/CS_Hacking.htm#edit_cbs), making it straightforward to develop a modern implementation.

## HERCs R Us
Sierra produced a collection of [89 custom .hrc](./downloads/89_Hercs.zip) files as a special release for Christmas 1996. Issue 29 of InterAction states that the files were created by Dynamix QA technician Matthew Vincent.

Without additional tools, `.hrc` files are difficult to effectively use or evaluate in single-player. If a player's technology level exceeds the HERC design, the imported HERC becomes underpowered. Conversely, if the `.hrc` file requires a higher tech level than the player has achieved, the HERC cannot be imported at all.

## Cyberstorm Demo
Sierra provided a free [promotional demo](./downloads/CyberStorm%20Demo.zip) of MissionForce: CyberStorm, available both as a downloadable release from the [Sierra website](https://web.archive.org/web/19970113114416/http://www1.sierra.com/games/cyberstorm/demo/readme.html) and on CD-ROM. The demo allowed players to experience three pre-made sample missions, though multiplayer functionality was not included.

## v1.1 Patch
[Patch v1.1](./downloads/v1.1%20Patch.zip) was a major overhaul for the game, introducing Hotseat multiplayer and Play-by-Email multiplayer support. It also rebalanced gameplay, particularly around the first Elite mission, added additional cheats and openly documented them within the game files, and introduced the Opportunity Fire mechanic, allowing both players and AI units to take reactive “overwatch” shots. Technically the update is named v1.10a; however, the community commonly refers to it as v1.1.

With the sheer number of improvements and gameplay refinements, v1.1 stands as the quintessential way to experience the game. No other updates or patches were officaly released by Sierra / Dynamix.

## v1.2 Homebrew Patch
The fans `Crow!`, `Seraphim`, `borg_down`, `siopaomanX` on [The Junkyard forums](https://web.archive.org/web/20121128141129/http://forums.the-junkyard.net/showthread.php/8480-Cyberstorm-Single-Player-V1.2-(Now-it-actually-works!)) created a ["v1.2" homebrew patch](./downloads/v1.2%20Homebrew%20Patch.zip) for the single-player campaign in 2007. The patch primarily focuses on increasing the game’s difficulty by modifying the equipment loadouts used by Cybrid enemies.

Special thanks for the dedication and expertise required to create such a patch. Rebalancing a complex strategy game at this level demands a deep understanding of its mechanics, enemy scaling, and overall campaign flow (Dynamix has 14 Quality Assurance Analysts listed in the credits). Truly legends!

## Windows Theme (Fan made)
Hosted on the [Official CyberStorm Site](https://web.archive.org/web/19970321071832/http://www.techline.com/~outlaw/guns/cs/) created by `RAtt` and `Lemming` is a downloadable [MSPlus Windows theme](./downloads/windows%20theme.zip).

No credits are attributed, however the theme appears to be reasonably well developed, featuring images, cursors, and sound effects taken directly from the game. For 1996, it is quaint and genuinely charming to see a fan-made Windows theme produced for the game, reflecting the era when desktop customization packs were a popular part of PC gaming culture. Sadly, there is no surviving context explaining how the assets were extracted or who specifically authored the theme. However, the startup screen links directly to the official CyberStorm fan site, making `RAtt` or `Lemming` the most likely creators.

# Lost Media
- `Crow!`'s documentation, `Cybrid Herc Design Listings.zip` and `Documentation.zip`, from [The Junkyard archive thread](https://web.archive.org/web/20150913221046/http://forums.the-junkyard.net/showthread.php/9780-Cyberstorm-Hexing-info). The documents reportedly contained instructions for modifying the game using a hex editor. ~2007
- In `Crow!`'s post publishing the v1.2 homebrew patch, he refrences "Seraphim's release of a very thorough description of the cybrid models has enabled us to locate the designs for the official Cybrid Hercs inside the CSTORM.EXE file." These documents apear to have never been published on The Junkyard forum or elsewhere. There is another refrence "I can't seem to find Seraphim's excellent Cybrid hacking spreadsheets online anywhere, so I'll repost them." however those documents were not followed up [on the thread](https://web.archive.org/web/20150913143342/http://forums.the-junkyard.net/showthread.php/9667-Cyberstorm-1-new-content). The thread also include lanaguge of playing as Cybrids (there is not a mention on how this is performed): 
> "You CAN, however, play the game as Cybrids. There are several bugs that need to be worked around to make this happen without crashing, but we have had several play by email games as either cybrid vs cybrid or cybrid vs human. I also played as Cybrids in the single player campaign, but it's absolutely brutal. A hit to a Cybrid damages all components equally, so that means a damaged Cybrid technically has a damaged life support. I highly recommend it if you're looking for a challenge." ~2007
- `dudejo` created a modified `.exe` featuring altered player weapon statistics. It was [published on The Junkyard](https://web.archive.org/web/20150127185830/http://forums.the-junkyard.net/showthread.php/9930-in-case-we-ever-find-how-to-change-weapon-stats), but the file itself was hosted on RapidShare. Recovery may prove difficult, as there is little identifiable branding or naming information to trace the upload. ~2010  
- [StormWatch Challenge details](https://web.archive.org/web/19970214174036/http://www1.sierra.com/games/cyberstorm/index.html). These were multiplayer tournaments with prizes supplied by Sierra. StormWatch Challenge #1 appears to have been canceled due to technical difficulties. StormWatch Challenge #2 appears to have been completed, though details such as the winners remain unkown. StormWatch Challenge #3 was [announced as “coming soon”](https://web.archive.org/web/19970615081413/http://www.techline.com/~outlaw/guns/cs/), but no further information has surfaced. ~1996


# Game Credits
**Executive Producer:** Jay Balakrishnan  
**Producer:** Graeme Bayless  
**Associate Producer:** Don McClure  

**Creative Director:** John Garvin  

**Lead Software Engineer:** Stephen Cordon  
**Software Engineers:** David McClurg, Miles Smith, Jimmy Campbell  
**Multiplayer Engineer:** Langdon Beeck  
**Additional Programming:** Christopher K. Singleton, Brian Danielson, Phil Taylor, Rhett Anderson, Dynamix "Darkstar" Engineering Group  

**Art Directors:** John Garvin, Mike Jahnke, Shawn Sharp  
**Art Resource Coordination:** Jay Dee Alley  
**Herc Designs:** Shawn Sharp  
**Production Artists:** Douglas Brashear, Barry Drew, Mary Ann Fernandes, Ron Clayborn, Point Asia  
**Additional Art:** Vance Naegle, Dan Buendia  

**Game Design:** John Garvin, Graeme Bayless, Don McClure, Robert Kraft, Stephen Cordon  
**Storyline:** Robert Kraft  
**Additional Writing:** J. Steven York  
**Assistant Director:** Robert Kraft  
**Scriptors:** Don McClure, Gerald Azenaro  

**Quality Assurance Manager:** David Steele  
**Quality Engineer:** Scott Gilbert  
**Quality Assurance Technician:** John Wolf  
**Quality Assurance Analysts:** Andrew Binder, Chris Stafford, Trish Bayless, Erinn C. Hamilton, Ben Nahorney, Alan Roberts, Aaron Anderson, Garrett Turner, Ken Eaton, Kenny Smith, Christa Wendland, Daniel Hinds, Gary Stevens, Matthew Vincent  

**Brand Manager:** Barbara Schwabe  
**Marketing:** Jaymi Bauer  
**Public Relations:** Barbara Dawson  
**Creative Services:** Heather Lavin  
**Packaging Art Direction:** Maria Mason  

**On-line Manual Writing:** Kevin Lamb  
**On-line Manual Graphic Design:** Egil G. Gløersen  

**Sound Engineer:** Ken Rogers  
**Music:** Loudmouth  

**Video Production:** James Carey, David Aughenbaugh