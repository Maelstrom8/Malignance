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

**Disclaimer: all of these mods are optional and not enabled by default for a reason. Some of them could invalidate a pawn, some could not. I don't really offer support for them past what is already written, whether it's a github readme, a mod note or a nexus modpage readme**.

## Optional Mods - Quick Merging Tutorial

Before you do anything, go to `tools` and extract `ARCTool Simplified` to a working directory. To install most of these mods, you need back up and then copy *one or more* of the archives within the `Output` folder, place it inside your ARCTool folder, and double-click **XFS_Extract**. You will have a loose version. These need to be overwritten by these respective mods - you do that by just copying them and replacing the originals here. After you do that, double-click **XFS_Repack** and put it back into the `Output` folder.

This is basically how I made a huge part of the list. 

## Optional Mods - Utilities

- [dinput8](https://www.nexusmods.com/dragonsdogma/mods/96) - A mod that can be viewed as an editor of some sorts. I don't use it but it could be useful. Required for [Greatsword MAX](https://www.nexusmods.com/dragonsdogma/mods/474).

#### Installation
- **dinput8** -- Just enable it, it's installed as a root mod. You will likely have to configure the settings. Pawn safe? No idea

## Optional Mods - Skills & Augments

- [Greatsword MAX](https://www.nexusmods.com/dragonsdogma/mods/474) -- A mod that overhauls Warrior skills. Requires dinput8. Probably cool, never used it
- [Better Augments](https://www.nexusmods.com/dragonsdogma/mods/1010) -- A mod I made that tweaks most of the augments, see the nexus page for more info

#### Installation

- **Greatsword MAX** -- Unpack the game_main.arc within the `Output` folder and replace `m_pl000_GSword.ajp` with the one from the mod (`Loose Mod Files\game_main\param\pl\other\m_pl000_GSword.ajp`). Enable the mod (due to it having a rom folder)
- **Better Augments** -- Unpack the game_main.arc within the `Output` folder and replace `PlAbilityParam.ablparam.xml` with the one from the mod (`Loose Mod Files\game_main\param\pl\other\PIAbilityParam.ablparam.xml`). You can enable it if you want but it doesn't NEED to be. Not pawn safe.

