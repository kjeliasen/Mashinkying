Mod structure
================================================================================
There is a strict directory structure in Mashinky's mod to help engine merge all
content on startup (or mod load). It is the same structure as in "/media/"
directory and all folders are optional in mods. 

config/ .. here all config files are stored
  accessories_types.xml .. accesories are some decorative objects in the game
          like track or road or stop endings, semafores etc.
  building_types.xml .. config file for all indutry and town buildings
  cargo_types.xml .. config file for all cargo types and tokens
  colors.xml .. config file for player colors
  face_types.xml .. config for recombinable faces in the game
  fonts.xml .. config file for font characters with texture coords and spacing
  headquarter_types.xml .. config file for player headquarter
  hints.xml .. config file with list of hint ids (from texts.xml)
  landscape_types.xml .. config file with different landscape types
  particle_types.xml .. config file for particle effects in game
  plant_types.xml .. config file for all vegetation types in game
  quest_types.xml .. config file for quests (using scripts in script folder)
  shortcuts.xml .. config file for key shortcuts in game (all gui IDs WBD)
  tcoords.xml .. all texture coordinates for GUI
  texts.xml .. localized texts with specific referenceable ids
  town_names.xml .. sets of town names
  track_types.xml .. config file for all track/road parts
  wagon_types.xml .. config file for all engines / wagons or other vehicles
map/ .. folder for all 2D assets (can be optionally stored together with models
          in model folder)    
model/ .. folder for all 3D assets
music/ .. music track in game (supported format *.ogg)
scenario/ .. all *.mss scenario files created in Mashinky's editor are stored herescript/ .. all LUA scripts used in game (config/quest_types.xml references
          these scripts)
shader/ .. binary compiled shaders used in game
sku/ .. optional folder where per language xmls are downloaded and combined
          together to config/texts.xml when reloading all ingame (using content
          creators window).
sound/ .. all sounds used in game

Mod tips
--------
- You may combine multiple mods into one by merging these folders and xmls
  together. This way your mod can add for example one engine, two wagons and 3
  cargo types at once
- All config xmls support multiple sections (like for example multiple 
  <WagonType> section in config/wagon_types.xml)
- In all "id" attributes, use unique generated hash (8x([0-9]/[A-F]) identifier
  like for example "108FA1C3"). When using existing hash (from other mod or base
  game content) you may overwrite any attribute of this item by your mod. When
  overwriting, use only attributes in your mod xml you want to change, 
  everything else stay unchanged.
- Some features may not be supported yet (like multiple landscape type). Check
  with our wiki pages or contact me on info@mashinky.com



Scenarios
================================================================================
In /scenario/ folder, you may store one or more *.mss files created in Mashinky 
ingame editor. You can find them in /media/scenario/ folder.
These files contains hand-made maps with industry preferred placement, towns, 
roads, vegetation or even track, bridges etc.

All together creates unique scenario providing new challenges for other players
as they can start new game on these maps.

You can also pack any other assets needed for your specific scenario into this
mod to keep it together



