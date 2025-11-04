<p align="center">
  [ <a href="https://github.com/Oghma-Infinium/Malignance/blob/main/README.md">Readme</a> |
  <a href="https://github.com/Oghma-Infinium/Malignance/blob/main/Documentation/GAMEPLAY.md">Gameplay</a> |
  <a href="https://github.com/Oghma-Infinium/Malignance/blob/main/Documentation/MODDING%20AND%20PAWNS.md">Modding & Pawns</a> |
  <a href="https://github.com/Oghma-Infinium/Malignance/blob/main/Documentation/OPTIONAL%20MODS.md">Optional Mods</a> |
  <a href="https://github.com/Oghma-Infinium/Malignance/blob/main/CHANGELOG.md">Changelog</a> |
  <a href="https://github.com/Oghma-Infinium/Malignance/blob/main/Documentation/FAQ.md">FAQ</a> |
  <a href="https://ko-fi.com/maelstrom_">Ko-fi</a> ]
</p>

# Modding & Pawn Documentation

There is a decent amount of things to cover here so grab something to drink, I dunno.

## Dragon's Dogma & Mod Organizer 2

Dragon's Dogma: Dark Arisen is not like other games, especially when managed through Mod Organizer 2. The game data is in the form of archives (.arc files) that need to be unpacked, edited and then repacked.

Mod Organizer 2 can actually manage the game fairly well, but there are mods installed in different ways, and I'll cover them below.

1) Mods that are installed normally, such as texture mods. An example is `Oblivion Armor - 4K`
2) Mods that are installed as loose files and enabled. They were already merged into the main archives. They do nothing as an enabled mod by itself. They exist to tell you that I use it. An example is `Easy Clothing IDs with HD Icons`
3) Mods that have one part of it that is installed normally, and another part that needs to be merged into some archive. An Example is `Dragon's Dogma Main Menu - Coils of Light`
4) All the mods in the optional mods category that are disabled, and even if enabled wouldn't do anything. They need to be merged and [require special instructions](https://github.com/Oghma-Infinium/Malignance/blob/main/Documentation/OPTIONAL%20MODS.md)


## Archive Files, Mods and You

You will see a lot of outfit and armor texture mods that are enabled. They overwrite smaller individual .arc files, they are typically textures or other things. These mods work as intended when enabled.

And then we have the ARCTool Output. This consists of these main archives: bbs_rpg.arc, bbsrpg_core.arc, game_main.arc and title.arc. It is essentially where the rest of the mods get merged into. 

These are the mods that were merged into the output:

- **10th Anniversary Loading Screen** is merged into bbs_rpg.arc and bbsrpg_core.arc respectively. 
    - Loose: `bbs_rpg\id\DDN\load\load01_ID.tex` and `bbsrpg_core\id\DDN\load\load01_ID.tex`
- **Dragon's Dogma Main Menu OST (Coils of Light)** is merged into title.arc. 
    - Loose: `title\sound\stream\bgm\Tittle_bgm.stq`
- **DDO Combat Music Project** is merged into bbs_rpg.arc
    - Loose: `bbs_rpg\sound\stream\bgm\bgm.stq`
- **Don't Blind Me - Medium Full** is merged into bbsrpg_core.arc
    - Loose: `bbsrpg_core\effect\tex\cm\t_cm000_00_GM.tex`
    - Loose: `bbsrpg_core\effect\tex\cm\t_cm040_00_GM.tex`
- **HD HP Custom GUI / Icon Overhaul** is merged into bbsrpg_core.arc and game_main arc respectively
    - Loose: `bbsrpg_core\id\cockpit\cockpit1_HQ_ID.tex`
    - Loose: `bbsrpg_core\id\minimap\mapicon_ID.tex`
    - Loose: `game_main\id\common\cate_icon\cate_icon_ID.tex`
    - Loose: `game_main\id\common\cate_icon\cate_icon00_ID.tex`
    - Loose: `game_main\id\common\job_icon_ID.tex`
    - Loose: `game_main\id\common\joutai_ijo_ID.tex`
    - Loose: `game_main\id\common\suji_ID.tex`
    - Loose: `game_main\id\minimap\mini_back_ID.tex`
    - Loose: `game_main\id\minimap\mini_mask_ID.tex`
    - Loose: `game_main\id\npc_wind\npc_mark_ID.tex`
- **Easy Clothing ID with HD Icons** is merged into game_main.arc. 
    - Loose: `game_main\dl1\id\common\item\combinedItemIcon_ID.tex`
- **Cleaner Female/Male Body Textures** is merged into game_main.arc and title.arc. Contains an update for HD Icons so it overwrites the others.
    - Loose: `game_main\models\` (too many to list)
    - Loose: `game_main\dl1\id\common\item\combinedItemIcon_ID.tex`
    - Loose: `title\models\` (too many to list)

**Some of the "enabled" mods do not do anything in Mod Organizer 2 if they are purely in loose form, as in they are an archive file unpacked - they are already merged, please don't touch any of them unless you know what you are doing**

---

### A Deeper Look Into Archives

Here are some examples of what is possible to edit when unpacking some of these archives. The archive file "game_main.arc" contains the following from my knowledge:

- Item Icons - `game_main\dl1\id\common\item\combinedItemIcon_ID.tex & .dds` 
- Quest Rewards - `game_main\etc\questReward\questReward.qr (.xml)` - This isn't the Notice Board, only the story quests
- Augment Effects - `game_main\param\pl\other\PlAbilityParam.ablparam (.xml)`
- Discipline Cost for Vocation Ranks - `game_main\param\pl\JobLevel\JobLvNAME.joblvl (.xml)` 
- Jump Height - `game_main\param\pl\other\PlJumpParam.ablparam (.xml)` 
- Carry Weight - `game_main\param\pl\weight\manyfileshere.plw` 
- Stamina Drain While Sprinting - `game_main\param\pl\stamina\PlStaminaDash.stm & PlStaminaDashAssassin.stm (.xml)`
- Experience Rate - `game_main\param\pl\level\exp.plexp (.xml)` 
- Weal and Prosperity - `game_main\param\status\player.statusparam (.xml)` 
- Stat Growth for Vocations - `game_main_param\pl\pl\level\LvNAME.lvl (.xml)` 

Advanced information on these could be found from some of my MME series mods. 

---

## Warnings - Mods vs Online Pawns

In Dragon's Dogma II, there is a clientside check for some things, and if you happen to get your pawn blocked it can be undone easily I believe. In Dragon's Dogma: Dark Arisen, I do not really much about this area. I did some testing with an alt with this modlist, and after I modified a Warrior augment, I couldn't see my pawn. It was Vigilance and I barely touched it.

Here is a checklist that I made from guesses and assumptions. I don't really know. If in doubt, set your pawn to private. [Pawn Share Settings](https://www.nexusmods.com/dragonsdogma2/mods/1057) mod for DD2 shows some insight on what the game checks for, so it might be similar to DD:DA.

### What could possibly invalidate / block a pawn from being seen

- Modifying the effects of the Augments of the six base vocations (Fighter, Warrior, Strider, Ranger, Mage, Sorcerer)
- Modifying the Stat Growth of the six default vocations ^
- Changing or giving max Knowledge to a Pawn
- Changing the cost of Augments
- Changing the DP cost for Vocation Ranks
- Using dinput8.dll or certain parts of it
- Changing the stats of base weapons / armor

### What doesn't invalidate / block a pawn from being seen

- Changing Carry Weight
- Changing Jump Height
- Changing Stamina drain while sprinting
  - It does not affect a pawn since they don't use stamina
- Changing Hybrid Vocations
  - It does not affect pawns because they don't use hybrid vocations
 - Changing Quest Rewards does not affect pawns in any way

## YO I WANT TO LEARN ABOUT THE OPTIONAL MODS

Not exactly the wrong documentation but you're looking for [this page](https://github.com/Oghma-Infinium/Malignance/blob/main/Documentation/OPTIONAL%20MODS.md).
