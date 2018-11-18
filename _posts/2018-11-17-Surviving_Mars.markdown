---
layout: game
title:  "Surviving Mars"
date:   2018-11-17 15:09:00 -0800
categories: game
downloadsize: 5.1GB
installsize: 5.3GB
bloatsize: 1.2GB
grade: C
gameversion: Steam OSX
---
The initial download size of Surviving Mars seems at odds with the low-poly low-res screenshots of the game. This is mostly explained by the resolution of the textures. They are larger than necessary for normal zoomed-out gameplay, but every pixel is visible when you zoom in to view your colony up close while playing at the highest settings, so this doesn't really qualify as bloat so much as artistic priority.

Despite this, about 1/5th of the download and install size of the game is unnecessary bloat.

The tutorial levels are stored as 16-bit heightmaps and 8-bit terrain type maps with lossless compression, half a dozen utterly unremarkable martian landscapes that you will likely never explore that take up 62MB each. The pre-sculpted terrain features like craters and mountains are stored similarly, as are various prefabs. Even slightly lossy compression would have reduced this 1.5GB of data to something closer to 500MB, and could have been subjected to artist/qa approval if there was some concern of artistic or gameplay integrity.

The main menu background has a simple looped video, a rotating sphere textured with the Martian surface, taking up 44MB. Rendering this in realtime would be trivial, unless the devs have intentionally disabled 3D rendering at this stage of the game to save cpu/power in which case kudos to them.

The images used in the UI are stored in TGA format, presumably for reasons of compatibility with the rendering engine. Storing them as PNG would save about 200MB.

The images used in the Encyclopedia are straightforward renders of existing game objects, taking up 87MB for images that could be produced at runtime and wouldn't need to be re-rendered by the artists when a patch changes a texture or model.

A measly 4MB is wasted on icons for PS4 players, which could have been omitted from this build of the game.

Everything described above could be resolved for both download and install size for a slight increase in game/menu loading time. They could also be resolved just for download size if they were unpacked/rendered once on first load or first use, which would probably be significantly faster than downloading them.

Breakdown of installed game contents:
- Packs
  - Maps - <span class="grade_D">1.3GB of pre-generated map and map chunk data</span>
    - Tutorial*.hpk - 62MB for each Tutorial level
      - height.grid - <span class="grade_D">~41MB heightmap (6145x6145 cells, 2 bytes per?)</span>
      - type.grid - <span class="grade_D">~21MB terrain types (6144x6144 cells, 1 byte per?)</span>
    - *.hpk - <span class="grade_D">same height and type density as Tutorial levels</span>
  - Textures*.hpk - 2.9GB of DDS-format model textures
  - UI.hpk - <span class="grade_D">377MB of TGA-format UI elements</span>
    - Messages - ~90MB background images for in-game messages
    - Encyclopedia - <span class="grade_C">~87MB pre-rendered images of game objects</span>
    - Icons - ~70MB exactly what it says on the tin
    - PS4 - <span class="grade_F">~4MB unnecessary PS4 controller icons</span>
  - Music.hpk - 300MB of Ogg Opus audio
  - Prefabs.hpk - 160MB of game entity data
    - *.h.grid *.t.grid - <span class="grade_D">similar to Tutorial*.hpk described above</span>
  - Meshes.hpk - 114MB of 3d model meshes
  - *.hpk - ~312MB of additional game assets
- Movies
  - Haemimont.* - 7.4MB logo video
  - Main Menu.ivf - <span class="grade_C">44MB video of a simple rotating textured sphere</span>
- Local - 36MB of localizations
- MarsSteam.app - 16MB game binary and a few libraries