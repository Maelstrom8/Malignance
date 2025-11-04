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
4) All the mods in the optional mods category that are disabled, and even if enabled wouldn't do anything. They need to be merged and required special instructions.


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

## Warnings - Mods & Pawns

**DISCLAIMER: BY READING THIS DISCLAIMER, YOU AGREE THAT IF YOU DON'T READ EVERYTHING HERE, CHANCE IS.. IT'S NOT MY PROBLEM**

I will cover which mods are safe for pawns, and which ones are not + which ones I am unsure about. In Dragon's Dogma, you can create companions called pawns, and you can share them online, where other people can rent them out and use them - which can benefit you the player as pawns have many mechanics to them. Most mods will affect pawns as they do you, because they use some of the same vocations, skills and systems. 

Any modifications done to a pawn that is considered "not-achievable" by legitimate means will result in a pawn being invalidated or basically, the pawn will show up as corrupt data and cannot be hired by others. You must start a new game to get around this.

### MODS THAT WILL INVALIDATE A PAWN OR WILL LIKELY DO SO

- Modifying the effects of the Augments of the six base vocations (Fighter, Warrior, Strider, Ranger, Mage, Sorcerer)
    - Eg. You change `Vigilance` to be give even ONE HP higher than it should. Doesn't matter.
- Modifying the Stat Growth of the six default vocations
- Changing or giving max Knowledge to a Pawn
- Changing the cost of Augments
  - Not confirmed but likely
- Changing the DP cost for Vocation Ranks
  - Not confirmed but likely
- Using dinput8.dll or certain parts of it
  - Not confirmed but definitely likely..
- Changing the stats of base weapons
  - Not confirmed but likely

### MODS THAT I DON'T THINK WILL INVALIDATE A PAWN

Considering that param modifications apply to both player and pawn, there are some that affect pawns in a literal way, but not in an online sense?

- Changing Carry Weight
  - Might affect them too but not confirmed if it invalidates a pawn
- Changing Jump Height
  - It affects a pawn in a literal sense but not confirmed if it invalides a pawn
- Changing Stamina drain while sprinting
  - It does not affect a pawn since they don't use stamina
- Changing Hybrid Vocations
  - It does not affect pawns because they don't use hybrid vocations
 - Changing Quest Rewards does not affect pawns in any way

## Notes on Pawn Invalidation

Invalidation of a pawn is only caused if you are playing with *certain* mods and have your pawn-sharing-status set to Online and someone else with the same mod finds your pawn (?). How the detection roughly works is that if you are not using a list, and are using for example.. an Augment tweak mod, it is totally fine client-side. The augments only change on your end, but once you send the pawn back, no mods are going through the server - because the other person doesn't have mods.. right?

NOW - Here's the funny thing. You are not safe to use these mods if someone hiring your pawn also has the mod. To explain further on that, if I decided to uhh.. archive some of these mods that invalidate pawns in the list, and some of you decided to hire each others pawns.. guess what? It is a game of how long until someone else using the list finds your pawn and well.. they both get corrupted! TRUE MULTIPLAYER

So again, if you want to use this mods and be safe, just set your pawn to private! This should cover everything but don't be afraid to ask questions.

## YO I WANT TO LEARN ABOUT THE OPTIONAL MODS

Not exactly the wrong documentation but you're looking for [this page](https://github.com/Oghma-Infinium/Malignance/blob/main/Documentation/OPTIONAL%20MODS.md).
