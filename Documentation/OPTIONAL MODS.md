<p align="center">
  [ <a href="">Installation</a> |
  <a href="https://github.com/Oghma-Infinium/Ascalon/blob/main/Documentation/Gameplay%20Documentation.md">Gameplay Doc</a> |
  <a href="https://github.com/Oghma-Infinium/Ascalon/blob/main/Documentation/Modding%20Documentation.md">Modding Doc</a> |
  <a href="https://github.com/Oghma-Infinium/Ascalon/blob/main/CHANGELOG.md">Changelog</a> |
  <a href="https://github.com/Oghma-Infinium/Ascalon/blob/main/Documentation/FAQ.md">FAQ</a> |
  <a href="https://ko-fi.com/maelstrom_">Ko-fi</a> ]
</p>

# Optional Mods Documentation

If you haven't read up on my previous documentation regarding things with modding and pawns, you [probably should](https://github.com/Oghma-Infinium/Malignance/blob/main/Documentation/MODDING%20AND%20PAWNS.md).

Be sure to use backups often.

**Disclaimer: all of these mods are optional and not enabled by default for a reason. Some of them could invalidate a pawn, some could not. I don't really offer support for them past what is already written, whether it's a github readme, a mod note or a nexus modpage readme**.

## Optional Mods - Quick Merging Tutorial

Before you do anything, go to `tools` and extract `ARCTool Simplified` to a working directory. To install most of these mods, you need back up and then copy *one or more* of the archives within the `Output` folder, place it inside your ARCTool folder, and double-click **XFS_Extract**. You will have a loose version. These need to be overwritten by these respective mods - you do that by just copying them and replacing the originals here. After you do that, double-click **XFS_Repack** and put it back into the `Output` folder.

This is basically how I made a huge part of the list. 

## Optional Mods - Utilities

- [dinput8](https://www.nexusmods.com/dragonsdogma/mods/96) - A mod that can be viewed as an editor of some sorts. I don't use it but it could be useful. Required for [Greatsword MAX](https://www.nexusmods.com/dragonsdogma/mods/474).

#### Installation
Just enable it, it's installed as a root mod. You will likely have to configure the settings. Pawn safe? No idea

## Optional Mods - Skills & Augments

- [Greatsword MAX](https://www.nexusmods.com/dragonsdogma/mods/474) -- A mod that overhauls Warrior skills. Requires dinput8. Probably cool, never used it
- [Better Augments](https://www.nexusmods.com/dragonsdogma/mods/1010) -- A mod I made that tweaks most of the augments, see the nexus page for more info

#### Installation

- **Greatsword MAX** -- Take game_main.arc from the `Output` folder, put it in your ARCTool folder, unpack it and replace `m_pl000_GSword.ajp` with the one from the mod (`Loose Mod Files\game_main\param\pl\other\m_pl000_GSword.ajp`). Enable the mod (due to it also having a rom folder that overwrites other archives that you don't touch but need to be overwritten)

- **Better Augments** -- Take game_main.arc from the `Output` folder, put it in your ARCTool folder, unpack it and replace `PlAbilityParam.ablparam.xml` with the one from the mod (`Loose Mod Files\game_main\param\pl\other\PIAbilityParam.ablparam.xml`). You can enable it if you want but it doesn't NEED to be. Not pawn safe.

## Optional Mods - Item Modifications

- [Shiny](https://www.nexusmods.com/dragonsdogma/mods/665?tab=description) - Adds stats to certain rings, I have the +25 version
- [End Game Element Swords 1H](https://www.nexusmods.com/dragonsdogma/mods/857) - Add elemental damage to certain end game swords

#### Installation

Both of these mods touch the same file (`Loose Game Files\bbs_rpg\etc\item\itemList.itl`). You need to pick between them, or else learn how 2 hex edit. Pick one, unpack the bbs_rpg.arc within `Output` and replace. 

## Optional Mods - Model Swaps

- [Barbarian Queen - Model Swap](https://www.nexusmods.com/dragonsdogma/mods/213) - Replaces several armors, see mod page
- [Black Brigandine - Model Swap](https://www.nexusmods.com/dragonsdogma/mods/483) - Replaces the Divine Surcoat with the Coat of Shadows' skirt.
- [Hellfire Armor - Model Swap](https://www.nexusmods.com/dragonsdogma/mods/596) - Replaces the criminally ugly ass endgame Hellfire Armor with various pieces, see mod page
- [Sinner Armor - Model Swap](https://www.nexusmods.com/dragonsdogma/mods/680) - Same as above

#### Installation

Just enable them. They function as normal mods, installed in a way they will overwrite specific files when enabled.

## Optional Mods - Other Texture Stuff

- [Hellfire Armor - 6K](https://www.nexusmods.com/dragonsdogma/mods/479) 
- [Chainmail (M+F) - 6K](https://www.nexusmods.com/dragonsdogma/mods/479)
- [Black Retextures](https://www.nexusmods.com/dragonsdogma/mods/5) 
- [Matte Robe](https://www.nexusmods.com/dragonsdogma/mods/925)

#### Installation

Just enable them. They function as normnal mods, installed in a way they will overwrite specific files when enabled. They might conflict with mods that touch the same textures/armors.

## Optional Mods - Core Tweaks
These are my set of mods that I made, they're basically common tweaks people like to make.

- [MME Series 1 - Sprinting Stamina Drain](https://www.nexusmods.com/dragonsdogma/mods/802) 
- [MME Series 2 - Carry Weight](https://www.nexusmods.com/dragonsdogma/mods/803)
- [MME Series 3 - Better Quest Rewards](https://www.nexusmods.com/dragonsdogma/mods/804)
- [MME Series 4 - Jump Height](https://www.nexusmods.com/dragonsdogma/mods/805)
- [MME Series 5 - Status Effect Tweaks](https://www.nexusmods.com/dragonsdogma/mods/1008)
- [MME Series 6 - Experience Tweaks](https://www.nexusmods.com/dragonsdogma/mods/1013)

#### Installation

Pick a version within each mod. Unpack the game_main archive within the `Output` folder, replace originals with mod files.

## Optional Mods - Offline Pawns

- [Pawn Stars](https://www.nexusmods.com/dragonsdogma/mods/87)

#### Installation

Just enable it. It functions as a normal mod, installed in a way it will overwrite a specific file when enabled. They are female only. You can additionally unpack this with arctool and edit it if you know how.

## Optional Mods - Other

- [Segmented Health Bar](https://www.nexusmods.com/dragonsdogma/mods/374) - Just visually segments enemy health bars

#### Installation

It's a loose mod. Take bbsrpg_core.arc from the `Output` folder, put it in your ARCTool folder, unpack it and replace the original `cockpit1_HQ_ID.tex` with the one from the mod (`Loose Mod Files\bbsrpg_core\id\cockpit\cockpit1_HQ_ID.tex`)

## The rest

I don't feel like going into the Ultrawide and Controller Support mods. I don't.. support them. Provided them anyway.
