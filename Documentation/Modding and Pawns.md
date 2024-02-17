<p align="center">
  [ <a href="">Installation</a> |
  <a href="https://github.com/Oghma-Infinium/Ascalon/blob/main/Documentation/Gameplay%20Documentation.md">Gameplay Doc</a> |
  <a href="https://github.com/Oghma-Infinium/Ascalon/blob/main/Documentation/Modding%20Documentation.md">Modding Doc</a> |
  <a href="https://github.com/Oghma-Infinium/Ascalon/blob/main/CHANGELOG.md">Changelog</a> |
  <a href="https://github.com/Oghma-Infinium/Ascalon/blob/main/Documentation/FAQ.md">FAQ</a> |
  <a href="https://ko-fi.com/maelstrom_">Ko-fi</a> ]
</p>


I will cover a lot of things involving how to mod the game, how mods interact, what the effects are, and other things. It will be a bit long so get some fuckin snacks and shit cause this is gonna be like the superb owl of documentation

## Dragon's Dogma & Mod Organizer 2

Dragon's Dogma: Dark Arisen is not like other games, especially when managed through Mod Organizer 2. The game data is in the form of archives (.arc files) that need to be unpacked, edited and then repacked.

Mod Organizer 2 can actually manage the game fairly well, and the mods for DD:DA are split into two groups, which is honestly just overwriting arc file(s)

1) Mods that start with a directory of /rom/ which will overwrite smaller arcs 
2) The "mod" or what I call the output, which is a directory of /rom/ and contain a lot the main game files such as game_main.arc, title.arc, bbs_rpg.arc etc

## Archive Files, Mods and You

You will see a lot of outfit and armor texture mods that are enabled. They overwrite smaller individual .arc files, they are typically textures or other things. These mods work as intended when enabled.

And then we have the ARCTool Output. This consists of these main archives: bbs_rpg.arc, bbsrpg_core.arc, game_main.arc and title.arc. It is essentially where the rest of the mods get merged into. Here is some examples - actually this is what has been merged into the output:

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

PS. I didn't mention this above, but uhm... considering my list isn't perfect.. the ARCTool Output also has the 'stages' from the base game copied into it, so it's a little bigger than it should and I'm not sure I needed to include these. The only mod I know that modifies the stage folder that i use is A Fortress Beieged but it only touches stage330.arc and not.. stage100-800 y'know? We'll leave it for now.

---

### A Deeper Look Into Archives

Here are some examples of what is possible to edit when unpacking some of these archives. The archive file "game_main.arc" contains the following from my knowledge:

- Modifying Item Icons - `game_main\dl1\id\common\item\combinedItemIcon_ID.tex & .dds` 
- Modifying Quest Rewards - `game_main\etc\questReward\questReward.qr (.xml)` 
- Modifying Augment Effects - `game_main\param\pl\other\PlAbilityParam.ablparam (.xml)`
- Modifying DP Cost for Vocation Ranks - `game_main\param\pl\JobLevel\JobLvNAME.joblvl (.xml)` 
- Modifying Jump Height - `game_main\param\pl\other\PIJumpParam.ablparam (.xml)` 
- Modifying Carry Weight - `game_main\param\pl\weight\manyfileshere.plw` 
- Modifying Stamina Drain While Sprinting - `game_main\param\pl\stamina\PlStaminaDash.stm & PLStaminaDashAssassin.stm (.xml)`
- Modifying Experience Rate - `game_main\param\pl\level\exp.plexp (.xml)` - I do not recommend
- Modifying Weal and Prosperity - `game_main\param\status\player.statusparam (.xml)` - LINES 289 AND 297, DEFAULT 300 (5 MINUTES)
- Modifying Stat Growth for Vocations - `game_main_param\pl\pl\level\LvNAME.lvl (.xml)` 

---

## Experimental Mods 

The extent of me allowing modifcations for my list is pretty much only the **Optional Mods** section and **this section**.

To get started, go to where you installed the modlist, under the `tools` section you will have a file called *ARCTool Simplified.7z* - Extract this to a separate folder, you will be using this to unpack and repack archives.

### Experimental Mods Cont.

You'll find four mods/folders here:

1. **DD:DA dinput8.dll hooks**: Essentially an editor It's required for Greatsword MAX and it will likely invalidate your pawn, but more on that later. It is installed as a root mod, so it can enabled without doing much else.
2. **Greatsword MAX** : A mod that reworks Warrior moveset/skills. Requires dinput8. To install, merge its `game_main` folder into your game_main.arc and then enable the mod and dinput8 if you want to use it.
3. **End Game Elemental Swords**: A mod I found recently that basically adds elemental damage to end-game weapons.. might invalidate a pawn. Might also be OP. To install, merge its `bbs_rpg` folder into your bbs_rpg.arc output.
4. **DD:DA Tweak Templates**: The meat and potatoes of messing around with gameplay parameters. It features many versions I made for modifying Jump Height, Carry Weight, Stamina Drain while Sprinting and Quest Rewards. None of these should invalidate a pawn but I'm not responsible if they do. To install, pick only one version if any, and merge their `game_main` folder into your game_main.arc.

Let's say that you hate sprinting costing Stamina, and you want it infinite. Head to `mods\DDDA Tweak Templates\Tweak Templates` and find the folder `Sprinting Tweaks` - pick the last folder labelled `Version 5 - No Stamina Cost`. Keep this explorer window active, but go to your ARCTool Output, find the **game_main.arc** file, copy it. Paste it into your folder you created for the ARCTool file and the other bat files. Double-click XFS_Extract, it should create a folder called game_main, a log folder, and another file for game_main responsible for telling itself how it's structured.

Go to the other explorer window for the `Version 5 - No Stamina Cost`, open it until you see **game_main** in folder form, copy this folder, paste it into the one you unpacked. It should overwrite the param files for Sprinting. Now double-click XFS_Repack. Wait. Take the newly created game_main.arc and replace it with the one in the output, done. 

BE SURE TO BACKUP YER FILES - I provided backups in `mods\DDDA Tweak Templates` if you fuck up.

---

## Warnings - Mods & Pawns

**DISCLAIMER: REGARDLESS OF MY "OBSERVATIONS" BELOW .. BY READING THIS DISCLAIMER, YOU AGREE THAT IF YOU HAVE A PAWN WITH THEIR STATUS SET TO "ONLINE" WHILE USING THESE MODS IN THE "EXPERIMENTAL" MODS SECTION, YOU ARE STILL RUNNING A POTENTIAL RISK THAT YOUR PAWN MIGHT GET BONKED AND IT IS NOT MY PROBLEM BECAUSE THE GAME IS LIKE 6 YEARS OLD LOL** - yes.

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
