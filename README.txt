Lilith's Throne
by Innoxia

Version 0.4.11.9 (exe version)

Compiled using Java version: jdk1.8.0_172

----------------------

IMPORTANT:

Please read the disclaimer before playing the game.

----------------------

HOW TO PLAY THIS GAME:

This game has only been tested on a Windows 10 operating system. I cannot guarantee that it will work on your system!

Simply double-click the file "LT.exe" to start the game! (This will only work on a Windows computer.)

----------------------

MISSING FOLDERS:

If you are getting warning messages pop up when you start the game (concerning not being able to read the 'data' or 'res' folders) then please try the following to fix the issue:

1. Make sure you have extracted the game from the .zip folder.
2. Make sure that the .exe file has write permissions enabled.
3. If the problem persists after the previous two steps, try moving your containing folder to a different location on your computer. Temporarily moving it to your desktop and running it from there is a good way to check that your system is able to run it correctly.
4. If the problem persists, please try joining the LT discord server and asking for help in the #tech-support channel.

If you use the command line or a batch/script file to start the game, please try starting it in the game folder to prevent this error.

---------------------

IMAGE QUALITY:

Some of the images of characters have been scaled down to reduce their file size. Due to the relatively small size of images displayed in-game, there should be no perceptible reduction in image quality, but if you would like to use character images in their maximum resolution, you can find the originals on the Lilith's Throne github: https://github.com/Innoxia/liliths-throne-public/tree/dev/res/images/characters

---------------------

PATCH NOTES FOR v0.4.11.9

Bugs:
	Fixed a background null pointer error from being thrown if you had slaves working in the brothel.

---------------------

PATCH NOTES FOR v0.4.11.8

Engine/Modding:
	Added an 'initSex' element to sex manager files, which is parsed at the start of the associated sex scene (a commented example is in res/sex/innoxia/managers/meraxis/duel/masturbation.xml).

Gameplay:
	Altered Youko pregnancy to fit with their lore: youko mothers will now always give birth to youko (if the father is not a demon), and youko fathers will follow standard rules for their children's race.

Sex:
	In ongoing penetration sex actions with more than two characters (such as two characters performing a blowjob on a third character), only the primary targeted character will experience orifice stretching effects.
	Sufficiently large clits now stretch orifices like penises/tails/tentacles do.

Other:
	You can now impregnate Shiranui during her sex scenes.
	Added the youko lore book, and a copy of the youko lore book can now be found in the dining area of Meraxis's hideout.
	Slightly adjusted some of the dialogue in Shiranui's mirror scene to put the explicit descriptions behind the 'keep watching' action, and made some minor tweaks to her dialogue elsewhere (such as her attitude when stealing your items and her comments at the end of the quest).
	Slightly rewrote some of Meraxis's new dialogue to make it more chuuni.
	If you get stripped by Shiranui, when you recover all of your items at the end of the quest, all of your flames will have been stolen by Shiranui (you will have the opportunity to get them back later on).
	If you correctly guess who Shiranui is, then the follow-up sex options (both solo and threesome) give you the option to transform her into a female or to transform into a futa Meraxis, as well as a double futa Meraxis option for the threesome.
	Added descriptions for the actions in Shiranui's cock worship sex scene and fixed issues with incorrect stretching mechanics.

Personality loss bug:
	NOTE: This bug only applies to saves which were saved in v0.4.11.6, so if you load an older save into this version then NPC personalities will be untouched.
	Fixed major bug where personalities of all characters were wiped when loading a saved game. All unique NPCs have had their personalities restored when loading into this version.
	All random NPCs will have their personalities regenerated as though they were newly spawned.
	To restore NPC personalities from an older save, either copy the 'personality' elements over from an older save or use the debug menu to set their personalities back to how they used to be, which can be done via:
	1. Standing on the same tile as the NPC
	2. Open debug menu by typing 'buggy'
	3. Navigating to the 'Personalities' tab
	4. Change the target to the NPC by using the first action button, then select the personality traits that they should have
	5. There is also an optional 'regenerate' action at the end of the list of traits, which you can use to regenerate the NPC's traits based on their race
	Sorry for the inconvenience.
	
Bugs:
	Fixed major bug where sex could sometimes crash when performing or receiving any of the following ongoing actions: anus-penis, vagina-penis, spinneret-penis, vagina-tongue, penis-mouth.
	Fixed major bug where slaves could not be assigned to the following jobs: lab assistant, test subject, prostitute, spa servant, spa clerk, waitress.
	Typo fixes.
	Fixed some parsing errors in the new Shiranui content.
	Fixed bug where (harmless?) background parsing errors could sometimes be thrown when generating offspring.
	Shiranui now correctly transforms back into her youko form after sex (when loading into this version, if she got stuck as a demon then she will revert to a youko).
	Fixed bug where when you exited Meraxis's hideout, the dialogue shown was for a generic Shinrin Highlands tile instead of the hideout tile.
	When choosing to have sex with Shiranui after correctly identifying her, Meraxis now correctly leaves the tile as is described in the dialogue (instead of awkwardly standing there as the two of you have sex).
	Fixed bug where the dialogue in Meraxis's hideout after having sex with her was that of the corridor in The Red Dragon instead of the corridor in the hideout.
	The table tile in Meraxis's hideout now correctly shows its own dialogue instead of that of the potion lab.
	Youko offspring will now correctly spawn with one tail.
	Fixed bug where Meraxis would always hate having sex with the player character if the player had been transformed into a demon by Lyssieth.
	Characters can no longer start autocunnilingus if they have a penis which is currently in use.
	Meraxis's 'Duel' and 'Sex' actions are no longer available in her hideout while she's sleeping.
	If you choose Shiranui's gifts instead of sex, the gifts will no longer disappear from your inventory when entering Meraxis's hideout (this was occurring if you had been stripped by Shiranui).
	Fixed bug in Angel's Kiss where if you whored yourself out, and the time passed the hour during this action, the NPC who arrived to pay you for sex was deleted from the game's NPC list, which made them appear not to be in the tile and which caused some minor issues with pregnancy and other stats.

---------------------

PATCH NOTES FOR v0.4.11.6

Engine/Modding:
	Added parser hooks for the Height, LabiaSize, ClitorisSize, LipSize, TongueLength, AssSize, HipSize, NippleSize, AreolaeSize, BodyHair, TesticleSize, and Wetness enums (using 'HEIGHT_', 'LABIA_SIZE_', 'CLITORIS_SIZE_', 'LIP_SIZE_', 'TONGUE_LENGTH_', 'ASS_SIZE_', 'HIP_SIZE', 'NIPPLE_SIZE_', 'AREOLAE_SIZE_', 'BODY_HAIR_', 'TESTICLE_SIZE_', and 'WETNESS_' prefixes, respectively).
	Stopped characters from being initialised twice when loading a game, which should hopefully speed up load times.
	Added a new ItemTag, 'USED_BY_BONDAGE_APPLIERS', which when added to a clothing type, makes it so that the clothing can spawn in bondage appliers' inventories (currently used for the latex catsuit and the latex hood).
	For modded races, added better error handling for if a null npc is detected while parsing the 'applySpeciesChanges' element.

Gameplay:
	Added the next stage of the main quest.
	Added Meraxis's hideout in the Shinrin Highlands (unlocked after completing the next stage of the main quest).

Youko's Mystery Potion:
	Added 'Youko's Mystery Potion' item, which can spawn in any tile where items can be randomly found.
	This item has a variety of effects, one of which will be randomly selected at the moment of consuming the item (so reloading your game and drinking the same potion a second time will have a newly-generated effect).
	These random effects are defined in 'res/randomEnchantments/potion', and can be added as mods by using the 'randomEnchantments/potion' directory, with a fully-commented example found in 'mods/innoxia/randomEnchantments/potion/cow.xml'.

UI:
	The character's quick overview tooltip (when hovering over your race icon or an NPC's race icon in the 'Characters present' panel) now also shows the character's age appearance.

Bodies:
	Added 'blue-grey' as an iris colour.

Other:
	Added a new 'Encounters' screen to the debug menu (button 13 in the 'Main' tab), which displays a list of all encounters that can occur in your current tile, and from that menu each encounter can be triggered via pressing a button.
	Adjusted the spawn rates of bondage-related clothing items in bondage appliers' inventories, so that they no longer spawn with latex clothing (except for latex catsuits and latex hoods) and they can now spawn with metal collars.
	Bondage fetishists will now sometimes spawn with chastity clothing and will equip this clothing onto their partners during sex.
	NPCs will no longer equip clothing onto their partners during sex if doing so would block an area that either they or any other character is interested in using (e.g. an NPC who's carrying a ballgag and wants to receive a blowjob during foreplay will now only equip the ballgag onto their partner after foreplay has finished).
	Denial fetishists will now spawn carrying chastity gear 50% of the time, which they will apply to their partners during sex.
	Yui now stocks 1-3 instances of each clothing type instead of only 1, and the metal collars she sells no longer have the enslavement enchantment.
	Adjusted the bonuses gained from the 'Arcane potential' and 'Arcane proficiency' effects (the tier 1 and 2 bonuses gained from your arcane being 10-30 and 30-50) from both giving +10/+10 spell damage/spell efficiency to +10/+5 and +15/+10.
	Themiscyra is now described as being occupied by Lunette's daughters instead of abandoned.

Bugs:
	Typo and parsing fixes.
	Fixed multiple instances of inconsistent descriptions while having a tauric lower body.
	Fixed bug where sleeping NPCs would react to you putting a condom on them.
	The 'latex catsuit' and the 'latex hood' clothing items can now be equipped during sex.
	Fixed incorrect description of pierced spider ears.
	Fixed incorrect description in prone bone sex scenes, where the orgasming character was described as looking down into their partner's eyes.
	When removing/adding personality traits, the description now correctly reflects whether or not the character already had/lacked the trait.
	Fixed bug where Ralph's discount would reset to 25% when starting any scene scene, and would reset to 0% when reloading a game.
	The 'All-out strike' combat move will now correctly strike with both arms (multiplied by the number of arm rows you have) when unarmed, instead of striking just once per arm row.
	Items with the 'breakOutOfInventory' element set to true, such as the Biojuice Canister, will no longer break out of an encounter and return to the tile's default dialogue when being used on an NPC.
	The 'Offspring using gender preferences' setting will no longer reset to the default option every time you restart the game.
	Fixed bug where the 'race reset' function in the debug menu wouldn't work properly after being used and then loading a saved game and trying to use it again.
	Fixed unintended behaviour where characters with an ovipositor could implant eggs inside an elemental.
	Condoms will no longer spawn with random enchantments on them, which was causing an issue where the condom wouldn't work correctly when equipped (you can still manually enchant condoms though).
	Fixed sibling and half-sibling detection in instances where character A's mother is the same person as character B's father and vice versa.
	Fixed background error being thrown when using the Offspring Map via a tile's response button instead of using it via your inventory.
	Fixed bug in the transformation menu where the '(Single)' option for udder count was unresponsive.
	The availability of hypnotic suggestion sex actions is now based on whether or not the targeted character has the 'Psychoactive Trip' status effect, instead of checking for psychoactive fluids ingested (so ingesting mushrooms will now correctly unlock the psychoactive sex actions).
	Fixed bug where if you started a new game after selecting a skin/covering colour in Kate's shop, that skin/covering colour would be available to be applied during character creation, even if it was meant to be restricted.
	If removing a place upgrade makes certain slave jobs unavailable, then slaves assigned to that job will now switch to IDLE during those hours in which they can no longer work that job.
	Tattoo counters with the 'written out' style now correctly display 'zero' when the associated count is 0.
	If you somehow manage to raise an npc attacker's affection without talking to them after defeating them in a fight (which should be impossible), then their name will be automatically revealed to you the next time you encounter them instead of forever remaining unknown.
	Fixed bug where if the fountain tile in Lilaya's mansion had the unlocked access to Lilaya's dungeon, then it wasn't possible to interact with a doll who was working as a statue on that tile.
	If you creampie Lilaya (in her half-demon form) with the sterile perk active and your virility at or below 0, she will now correctly stop sex (as she couldn't know that you're completely sterlie and so should act as though you might have got her pregnant).
	Fixed bug in the pregnancy stats screen in the phone menu where if the eggs that you implant inside yourself were conceived as a result of self-impregnation, then the total number of offspring would be incorrectly doubled, and a related bug where implanted offspring were not being counted towards the sons/daughters mothered count at the top.
	Demons which are turned into slimes are no longer limited to demonic transformations, but can transform in all the ways that a normal slime can (and when/if transformed back into flesh, they will revert to a demonic form).

---------------------

PATCH NOTES FOR v0.4.11.3

Engine/Modding:
	Added 'PRESCRIPTION_GLASSES' as an ItemTag, which grants any wearer a small status effect buff ('enhanced vision'), and also negates the 'impaired vision' effect which affects characers with the 'visual impairment' perk.
	Added 'EYE_PERFECT_VISION' as a BodyPartTag, which makes the character immune to the negative effects of the 'impaired vision' perk. (Demon, angel, dragon, gryphon, and raptor eyes have this tag.)
	Added 'breakOutOfInventory' element to item types, which is false by default, but when true it causes the inventory to close when using the item (commented element in 'res/items/innoxia/pills/fertility.xml').
	Converted money from integer values to longs (in case the player manages to somehow earn more than 2.1 billion flames).
	Added a new TFPotency, 'SPECIAL', which when used as the potency on an item of clothing's sealed item effect will make it impossible to unseal. See the 'game/inventory/enchanting/TFPotency.java' file for comments on this and application details. (This will not be present nor available in a normal game; it's been added for use on special modded clothing.)
	Added support to combat moves for hitting multiple targets and improved the formatting for several elements (the old formatting still works, so there's no need to update moves to the new format); a fully commented example is in 'res/combatMove/innoxia/quadruped_kick.xml'.

UI:
	Improved the appearance of the race page in the encyclopedia and added ability to click on race entries to open their subspecies info page.
	Additional descriptions in clothing tooltips (things like 'sex equip enabled' or 'fits arm-wings') now continue to be shown when the clothing is equipped.
	Improved character's quick overview tooltip (when hovering over your race icon or an NPC's race icon in the 'Characters present' panel) to show femininity, body shape, and height at the top underneath their race's name, and also neatly cut off text overflow with an ellipsis.

Gameplay:
	Slime and elemental transformations now require advanced knowledge of races (obtained from race books) in order to transform into them.
	The subspecies which newly-spawned slimes decide to mimic are now limited to the subspecies found within their region (e.g. slimes spawned in Submission will spawn as subspecies which can ordinarily be found in the region of Dominion, which encompasses all of Dominion and Submission).

Impaired vision:
	Added 'visual impairment' as a new unique perk, which gives a negative status effect while not wearing clothing with the 'PRESCRIPTION_GLASSES' tag (i.e. glasses).
	randomly-spawned NPCs having a 2.5% chance to have it (there is no way for the player to get this perk at the moment but I might add a way to get it later on).
	Nizhoni, Vanessa (Ms. Cunningham), and Ziva (Ms. Levine) now have the 'visual impairment' perk.
	If a character has the 'visual impairment' perk, any clothing with the 'PRESCRIPTION_GLASSES' tag (i.e. glasses), will not be removed at the start of sex if 'Automatic stripping' is enabled, and selecting 'unequip all' in their inventory will also ignore any clothing with the 'PRESCRIPTION_GLASSES' tag.

Items:
	Using the 'bioslime canister' now breaks out of your inventory, making it easier to see the full transformation text.
	
Sex:
	Added 'lying on front' as an alternative slot to 'lying on back' in the 'Lying down' sex position, which allows partners to perform oral, receive oral, or have sex in the 'prone bone' position.
	The 'beside' slots in the 'Lying down' sex position now have correct interaction availability with characters lying down and those in non-lying-down slots.
	Added the new 'prone bone' position as an option to switch to during sleep sex.
	Improved dirty talk lines and positioning descriptions for when used in sleep sex.
	Removed the Hypermobility perk's non-taur requirement for being able to perform autofellatio & autocunnilingus (so taurs can now perform those actions if they have the hypermobility perk).
	
Other:
	Added 'Craft x5' and 'Craft all' options to the enchantment menu to make bulk enchanting a little less tedious.
	Increased the threshold for additional inventory slots being dirtied by cum when a character orgasms onto their partner; additional slots being dirtied now starts at 30ml of cum instead of 16ml, and not as many slots are dirtied (but the maximum cum bracket of 1,000-10,000ml is unchanged at 8 slots dirtied).
	Slaves assigned to your bedroom, who are attracted to you, and who have permission to sue you, will now engage in sleep sex with you (if you have the heavy sleeper perk) at least once in each block of bedroom work they're assigned to (a block being any number of consecutive hourly slots).
	Increased maximum height in character creation screen from 200cm to 215cm (so you can start as 7 feet tall).
	
Bugs:
	Parsing and typo fixes.
	Removed the 'Back' button from the initial dialogue when starting a new game, as returning to the main menu and then trying to resume from there would throw errors.
	You can no longer unequip/equip/unseal clothing nor use items in a sex scene in which you are immobilised.
	Fixed bug with frotting, where if you were targeting a different character to the one you were frotting with and selected the 'Frotting orgasm', the cum effects would be applied to the targeted character instead of the one you were frotting with.
	Fixed bug in the encyclopedia, where if the horse shoes were discovered, the 'feet' clothing section would display an error message (if this bug was occurring in other pages, they all should be fixed now).
	Fixed job selection perk tooltips displaying the player's currently selected occupation instead of the perk's associated occupation.
	Fixed bug where you could get stuck in an infinitely-looping menu if you opened your phone while in the Enchantment save/load dialogue.
	Fixed incorrect orgasm description in group sex which occurred when character_A gave character_B a creampie while targeting character_C.
	Fixed game-breaking bug where the game would lock up if any sex actions were started with a character who had an ovipositor penis or an ovipositor clit.
	Fixed bug where NPCs who transform you after sex would alternate between shrinking and growing your breasts and/or crotch-boobs.
	When setting an unemployed friendly occupant to a job within the manor, the occupant/slave overview list will now show the same income information which is in their job dialogue, instead of always showing 0/day.
	Fixed bug where opening a friendly occupant's inventory via the overview menu's inventory button would sometimes cause the inventory to get stuck, soft-lock your game, and throw background errors.
	Fixed clothing tooltips not displaying all of the clothing's extra information.
	Fixed the 'slaves' in Slaver Alley's cafes not actually being set to being slaves, and having incorrect descriptions as a result.
	Corrected multiple inconsistent pregnancy descriptions for if you're a taur.
	Fixed bug where dolls (including the player) would have their aura set to NaN (also fixed the same bug for health values).
	Fixed some formatting bugs in the newly updated tooltips.
	Fixed nipple and crotch-nipple creampie retention enchantments not working.

---------------------

PATCH NOTES FOR v0.4.11.1

Additional note:
	The 'res/images/characters' folder has been reduced in size (from ~390MB to ~100MB) by scaling the larger images down to a maximum height of 1080px. If you want the originally-sized images, then you can get them from the github repository.

UI:
	Removed the 'Enchantment instability' text above the inventory UI panel to stop it from wrapping onto a new line if instability was over 99 (the new icon for Enchantment instability should make it clear what the numbers mean anyway).
	Updated the tooltip formatting to align with the new item tooltip formatting for: status effects, perks, combat moves, fetishes, desires, spells, and spell upgrades.
	The 'Items Present' panel is no longer greyed-out when in the inventory screen.

Gameplay:
	Added ability to fuck Vronti's ass (unlocked after having previously given him a blowjob or performed anilingus on him).
	Added ability to continue seeing clients in Yui's dungeon scene instead of having the night skip to the end after the first client, and added a random variation for the client's into scene.

Sex:
	Further refined the condom orgasm behaviour of NPCs, so NPCs wearing condoms will no longer pull out of orifices if the condom is going to break (as they don't know in advance that it's going to break), but if they aren't penetrating an orifice, then they are free to choose an area of their partner to cum onto as the condom breaks.
	Split actions involving tail egg-implanting, so that if a character is penetrating multiple orifices by using multiple ovipositor tails, they now get the option to implant eggs any of the penetrated orifices, instead of the orifice being randomly selected.

Other:
	Applied tagging to character images so that character artwork which was spread across multiple folders is now all located in one folder (applied to Fae, Silvia, Shadow, Silence, Fyrsia, Hyorlyss, Jess, Lyssieth, Meraxis, Nyan, Leotie, and Takahashi).
	Fennec-morphs no longer need dirty blonde, bleach blonde, or tan fur to be identified as a fennec-morph, and instead just require fennec fox ears.
	Changed Rose's cat-fur colour from black to light red (which was her intended colour as can be seen in her artwork; I didn't realise it was black in-game this whole time...).

Bugs:
	Typo and parsing fixes.
	Fixed major bug in sex where sometimes the action buttons would become unresponsive and the game would soft-lock.
	The enchantment instability tooltip should now correctly display when hovering over an NPC's instability count (i.e. the panel directly above their inventory when managing their inventory).
	Fixed parsing errors being thrown if you loaded a save in which slaves had the 'broodmother pills' permission assigned to them.
	Fixed bug where you couldn't use a tail ovipositor to lay your eggs in your own womb (surely the biology works somehow...).
	Fixed cause of parsing errors and background errors being thrown when a pregnant character's litter was checked to see if another character was the father, but the litter's father had been removed from the game.
	Fixed error being thrown during sex when performing this sequence of moves: start sex with sealed clothing, unseal & remove that clothing, re-equip that clothing, and then attempt to unseal it again.
	Fixed a bug where the shared encyclopedia was not being applied correctly, and additionally the shared encyclopedia is now updated whenever loading a game (to make sure that all of your discovered items/clothing/weapons/races are added to it).
	The 'On the pill' status effect which Alexandria (the woman in the prologue) has now correctly makes it so that she's unable to get pregnant.
	Scarlett's and Brax's slave collars will no longer have duplicate sealing enchantments.
	Fixed bug where NPCs who transform you after sex would constantly try to shrink your breasts and/or crotch-boobs even if your breasts/crotch-boobs were as small as possible.
	Kate will no longer stop you from putting on a condom if she's asleep.
	Added missing tooltip to the 'bar' upgrade for the spa (which was missing only after it was built).

---------------------

PATCH NOTES FOR v0.4.11

Contributions:
	Consolidated the TF race methods and layout dialogues in the BodyChanging class. (PR#1808 by Maxis010)
	Fixed a lot of typos and parsing errors. (PR#1799 by CKRainbow)
	Fixed a lot of typos and parsing errors. (PR#1789 by Simones112)
	Added ability to directly parse an item within its own description. (PR#1438 by CognitiveMist)
	Fixed bug where modded combat moves were not implementing the blockAmount tag. (PR#1851 by miome)
	Fixed some races being incorrectly named 'winged-race'. (PR#1839 by Stadler76)
	Improved handling of RESTING_LUST attribute calculation, so any effects which lower resting lust should now have the correct effect. (PR#1788 by SightglassCat)

Multiple fixes from #PR1778 (by Maxis010):
	Added +/- 100 buttons to sex experience for character creation. (Innoxia: I also made some changes to the formatting of the sex experience dialogue.)
	Fixed bug where characters could sometimes exceed the intended level cap.
	Added some checks to prevent Integer overflows.
	Nerfed level drain so the character draining experience now receives an experience amount of 5x the target's true level.
	Slightly increased the amount of flames generated from milking slaves, by rounding the number of flames earned per hour up to the nearest integer instead of down.
	Added a null check to subspecies loading to fix a potential softlock when loading a subspecies that had incorrectly-defined attributes for its associated status effect.
	Added a warning to the main menu if the game detects that you're running it from within a temporary directory (which indicates that you haven't unpacked the .zip file). (Innoxia: I also made a slight change to the 'Last Save' formatting on the main menu.)
	Fixed some typos and made a few descriptions in the options screen a little clearer.
	Added a small java version warning to the main menu if the game is being run in a java version other than 1.8.0_172.
	Bondage fetishists can now spawn with items from the Latex set (and won't spawn with slave collars anymore).
	Added a confirmation check to the action to restore default values in the options menu for gender pronouns and gender, orientation, age, furry, and fetish preferences.
	Fixed bug where it could be possible to alter furry and spawn preferences for races which are meant to be unalterable.
	Fixed bug where submission attackers were spawning as a slime or an imp more often than was intended.
	Fixed bug where the affection changes applied from a slave interaction 'molest' scene didn't match the dialogue.
	Fixed bug where brothel visitors would not leave.
	Fixed bug where tails could be incorrectly marked as Suitable for Penetration in the transformation menu (which was affecting raptor and pig tails).
	Consolidated repeating code in alleyway encounters into a single method, and added the ability to use the offspring map directly from an action (always on the second action button) while on tiles which support the offspring map. (Innoxia: Fixed a bug where the offspring map was sometimes not able to be used when it should have been available.)
	
Frotting actions (PR#1782 by Sightglass):
	Added frotting as a new type of ongoing action for penis-to-penis interations.
	Added an associated frotting orgasm, special actions for sheath-docking and prehensile-penis interactions, a couple of sadistic actions for SPH, and a speech action to compliment your partner's cock.
	Added cloacal penetration while engaged in ongoing frotting.
	
Engine/Modding:
	Added a 'REMOVE_FROM_DRESSING_ROOM_OUTFITS' item tag to prevent weapons or clothing from being available in the dressing room outfit creator.
	Added temporary boolean, String, and int variables to the DialogueFlags class, which can be accessed via the 'flags' parsing target, and used via getter/setter methods getBool(String id), setBool(String id, boolean value), getString(String id), setString(String id, String value), getInt(String id), setInt(String id, int value). The temporary variables which you set via these methods are forgotten whenever a game is loaded; they're intended for use across multiple conditional checks within a game's instance, not for saving data to the game's file.
	As part of PR#1438, clothing, weapon, and item mods can now parse a reference to themselves in their descriptions by using the 'thisItem' parsing target, and can also parse the owner of the item with the 'npc' target (which should use a null check to be used) - comments have been added to the example XML files to describe this.
	Added 'appendEnchantmentPostfix' as an optional attribute to clothing's name element (defaults to true if omitted), which when set to false will prevent an automatically-generated enchantment naming postfix from being appended to the end of the clothing's name.

UI:
	Reformatted tooltip content for clothing, weapons, items, and tattoos, to fix several issues with readability, content being cut off, and lots of wasted space.
	When your inventory is disabled (such as in most scenes where you also can't move freely), the 'Items Present' UI panel on the right is now visibly disabled.
	Renamed 'enchantment capacity' to 'enchantment instability' to make it clearer that it's a negative aspect when associated with enchanted items.
	Enchantment instability is now shown in the main dialogue panel when displaying details about a selected weapon or clothing.
	Fixed tooltip formatting of modifiers in the enchanting menu, so you can now correctly see the modifier's essence cost when hovering over them.
	Fixed bug where very tall tooltips would cut off content at the bottom.

Gameplay:
	After installing Lyssieth's wardrobe in your dressing room, a short voyeur scene is unlocked on Rose's room tile (available whenever Rose and Lilaya are present there, which is between 22:00-06:00, and can be repeated after 7 days have passed since last viewing it).
	You can now only self-transform slimes and elementals (either yourself or NPCs) into races which you've previously discovered (which takes into account your 'shared encyclopedia' setting).

Random enchantments:
	Random enchantment added to items of clothing found in alleyways have been reworked.
	Negative enchantments will now be either one of 28 new themed enchantments, most of which involve transformations, or they'll be a more impactful generic enchantment (75% chance for them to be one of the uniquely-themed enchantments).
	Positive enchantments can similarily be drawn from one fo 7 new themed enchantments, or be a more generic bonus.
	Instead of negative & positive enchantments both having a 20% chance to spawn, negative enchantments are now 30% and positive are 10% (with a 60% chance for clothing to not be enchanted).
	These custom-made random enchantments are defined in 'res/randomEnchantments', and can be added as mods by using the 'randomEnchantments' directory, with a fully-commented example found in 'mods/innoxia/randomEnchantments/clothing/cow.xml'.
	
'Filly' reference change:
	All references to 'filly' in Natalya's content have been replaced with 'mule'.
	The 'filly choker' now has two sticker options for the text on the choker; the default is now 'mule', and the alternative is 'filly'.
	If you change the mule choker's sticker from 'mule' to 'filly', all references to 'mule' within the game will revert to 'filly', so if you don't like this 'mule' change, just swap the sticker on your choker to revert to the previous filly references.
	<i>Innoxia's note: I used 'filly' as I wanted a horse-related term which would be demeaning, but I've seen feedback in several places from players saying they were uncomfortable with this term, so I thought 'mule' was an acceptable replacement.</i>

Clothing & tattoos:
	Added 'beanie' clothing (androgynous femininity, head slot, sold by Nyan, can spawn on generic muggers in Dominion, Submission, and Elis).
	Added 'gender glyph' earrings (ear piercing slot) and barbells (navel and vaginal piercing slots), of the 'male', 'female', and 'herm' varieties, each with a 'circle' or 'heart' sticker variation (masculine, feminine, and andgrogynous femininity, respectively. Sold by Kate.).
	Added tattoo types: 'male', 'female', and 'hermaphroditic' glyphs.
	Added tattoo type: 'penetration ruler' (can only be equipped into the 'lower abdomen' slot).
	Added two stickers to the new 'latex hood' clothing item, which allow you to remove the eye and mouth holes.
	When enchanting clothing, the 'Vibration' and 'Orgasm prevention' enchantment modifiers are now accessed via selecting a new 'sexual effects' enchantment modifier as the primary modifier, instead of 'Special effects'. (This change is to make it more obvious when the vibration & orgasm denial effects are available, as they're not available/visible on all clothing items.)
	If clothing has multiple seal enchantments on it, the cost to unseal it will now be the sum of all of them.
	Randomly-spawned clothing of the rarities 'uncommon', 'rare', and 'epic' now also have a chance to spawn with a random enchantment.
	Moved all remaining torso clothing from being hard-coded into xml files (into the 'res/clothing/innoxia/torso' folder).
	The 'cami top' is now correctly marked as leaving the wearer's stomach exposed.
	Increased values of some clothing: skater dress 250 -> 400, virgin killer sweater 100 -> 800, frontal-zip dress 350 -> 500.
	The default enchantment on the 'Mega Milk T-shirt' has been changed from '+3 to physique' to hourly increases to breast, nipple, and areolae size, and to lactation amount and lactation regeneration.

Sex:
	Natalya and Thunder (the centaur involved in her training scenes) no longer allow you to use items or equip condoms on them in their sex scenes.
	If an NPC's condom will break when orgasming, then they can now use all available orgasm actions (before this change, NPCs would not make use of the fact that their condom breaks, and were likely to use a generic orgasm action instead of one drawn from their preferences).
	Sex actions should now have a more consistent ordering, especially for start/stop ongoing actions.

Other:
	You can now only have one dressing room upgrade at a time, and after paying to have Lyssieth's wardrobe re-enchanted, it will be automatically installed if you remove your dressing room and then add it again.
	Added an 'On the pill' status effect to Alexandria (the female NPC in the prologue), as well as a brief line for her to mention it, thereby giving a reason for why you're always told that there's no chance of getting her pregnant if you creampie her.
	You can now find 'epic' rarity clothing in alleyways, at a lower chance than other rarities.
	Increased the cost of identifying clothing from 400 flames (at a shop) or 3 essences (to do it yourself), to 1000 flames or 15 essences.
	You can now identify unidentified clothing when it's on the ground.

Bugs:
	Typo and parsing fixes.
	Fixed incorrect description when ending an ongoing tongue-to-nipple sex action, where the tongue was described as being taken 'out' of the target's nipple even if the nipple was not penetrable.
	Added in a line to give a brief, generic description when changing position in sex via the positioning menu.
	Fixed a bug where Kate was supposed to prevent you from using condoms on yourself during her sex scenes, but the conditional check was always bypassed.
	Fixed bug where Thunder (the centaur involved in Natalya's training scenes) could sometimes spawn with a lisp.
	The title at the top of the UI in sex scenes will now update to display the name of the currently selected sex position, instead of always displaying the initial position's name (unless the sex scene has a unique title, in which case it will continue to display that).
	In Ralph's 'big discount' sex scene, the positions will correctly update to show that you're bent over his desk, instead of always saying you're kneeling under it.
	Fixed postfixes added to default clothing names based on fetish enchantments to read 'of the X' instead of 'of X' (e.g. An enchanted ring now reads 'Silver ring of the submissive' instead of 'Silver ring of submissive').
	Fixed bug where if an arcane storm started on the same turn that you met a random mugger, the option to pay them off would appear available but not actually work.
	Fixed the clothing names in the 'Items Present' panel being displayed as their generic name even if they had a custom name.
	Fixed bug where attempting to enchant an item of clothing with crotch-boob creampie retention would throw background errors and make the enchanting UI break.
	Fixed issue in the new floor inventory UI, where an extra page would be available to be viewed when the previous page was full, even if this new page was empty.
	Fixed a bug where if you had the maximum number of slaves working as dairy cows, the ability to assign their working hour slots would become unavailable.
	When creating outfits in Lyssieth's wardrobe, liquids enchantment limits now correctly increment by 500 instead of 5 when the large limit change button is pressed.
	Fixed bug where the stickers on clothing within saved outfits in Lyssieth's wardrobe were not being initialised correctly, so if you edit an item with stickers, the buttons should no longer all be greyed-out.
	Fixed minor error in sticker definitions within the new latex hood clothing item.
	Fixed parsing error in post-combat loss scene with bandits in the Foloi Fields.
	Fixed buggy comparison function in TattooType.getAllTattooTypes().
	Fixed incorrect sex positioning when giving a blowjob to Vronti.
	In the Vronti handjob scene, you can no longer switch to giving him a blowjob unless the 'blowjob' action has already been unlocked in the previous scene.
	The maximum amount of unique clothing and weapons sold by Vicky are no longer limited by the number of unique items, essences, and spell books which she sells in her 'item' tab.
	Fixed bug where you could not interact with the three demonic leaders of the fortresses in Submission after defeating Meraxis.
	The the character creation process at the start of the game, the colour of your equipped piercings will be preserved if you leave the inventory dialogue and then return to it.
	Fixed bug where if you had clothing equipped which prevented orgasms, then using the 'quick sex' action would cause the game to crash.
	Fixed some parsing errors in the 'mag dump' special moves which would occur if you didn't have enough essences to use the special move.
	Fixed bug where demons and other races which don't age could sometimes spawn with a birthday in the future.
	Fixed bug where when applying outfits to yourself or your slaves, clothing which should be discarded upon unequipping it (such as the tape items) would instead be placed on the floor.
	
---------------------

PATCH NOTES FOR v0.4.10.9

Pusspuss's Artwork (https://twitter.com/PusspussARTZ):
	Added Hannah artwork (with pregnant variations, multi-breast variations, and different variations based on whether you're seeing her in the gym or in the bar, Light's Out).

FriendlyAlienFriend's Artwork (https://twitter.com/thealienfriend):
	Added Natalya artwork (with pregnant and crotch-boob variations, although neither of these extra variations are currently seen in-game).

Engine/Modding:
	Character sex preference code is now parsed on each call instead of once when initialised, allowing you to make more complex sex preferences.
	Added 'FITS_BIPEDS' as an item tag to allow clothing to be tagged as only being able to fit bipedal bodies.
	Added a 'category' element to custom sex actions, allowing you to set which response tab you want your action to be placed into.
	Added a parser hook for LubricationType, using the prefix 'LUBRICATION_'.
	Potency values are now correctly applied to the generated attribute when defining 'RESISTANCE_WEAPON' and 'DAMAGE_WEAPON' enchantment values for modded weapons, instead of always being TFPotency.MAJOR_BOOST.
	Added 'essenceFormat' parsing command which works the same as 'moneyFormat' but for essences.
	
UI:
	Changed the essence icon from an embedded image to the unicode pentagram symbol to make the UI look more consistent (also the inline image was awkward to format in css).
	
Gameplay:
	Re-enabled feral impregnation, with the offspring of ferals now always being the tauric equivalent of the mother (e.g. centaurs for feral horse, driders for feral spider, etc.).
	Added a small amount of extra content for Yui (the demonic spider-girl in the Farmer's Market in Elis) - after choosing to 'Get dominated' by her, a new action, 'Beg for more', will lead into the new content.
	After having sex with Callie once, you can now directly give her donations to progress to the next level of her store upgrades.
	Added a small piece of content for Callie's shop, 'The Creamy Bakey'; if you've completed Natalya's quest, are wearing a filly choker, have performed anilingus on Callie at least once, and have upgraded her shop to the maximum level, then when entering her store you can encounter Natalya in there and have an anilingus-focused threesome.
	Added a new option, 'Offspring using gender preferences' (accessed via 'Content options'->'Gender preferences'), which allows you to define whether or not you want offspring to use your preferences when determining their gender.

Outfit feature:
	Added 'Dressing Room' as a new room upgrade in Lilaya's mansion, which can be upgraded with 'Lyssieth's wardrobe', which gives you access to a new outfit feature.
	You can create, edit, save/load outfit files and then purchase an instance of your created outfit to equip it to yourself or any of your slaves.
	Outfit files are saved in the 'data/outfits' folder (not to be confused with 'res/outfits', which handles a different type of outfit generation on NPC spawns).

Inventory:
	Floor tiles now all have unlimited inventory space.
	All weapons, clothing, and items which have a rarity of 'Quest' are now sorted to always be at the top of the 'Items Present' list.

Clothing:
	Added 'latex catsuit' clothing item (epic rarity, torso slot, 'latex lover' clothing set, sold by Saellatrix).
	Added 'latex hood' clothing item (epic rarity, torso slot, 'latex lover' clothing set, sold by Saellatrix).
	The 'full chastity belt' clothing item now correctly blocks access to the wearer's anus.
	Slightly updated the 'blazer' clothing image, limited the colours which it can spawn as, and added secondary and tertiary colouring options.

Items:
	Added 'lube pill' item (lubricates entire body in sex scenes, sold by Ralph).
	Slightly improved icons for pill items.
	
Sex:
	Made some minor improvements to the resisting variations when asking an orgasming partner to pull out.
	Added a small change to the 'Orgasms' status effect icon and text when the linked character is satisfied from the number of orgasms they've received during the sex scene.
	When unrestricting control of a submissive partner in sex, if they decide to then immobilise you (via constriction, cocoon, or Witch's Seal), you now retain the ability to modify their permissions and to stop the sex scene.
	NPCs with a positive desire towards the 'cum stud' fetish no longer always choose to creampie.

Slave management:
	Non-doll slaves can no longer be assigned the 'statue' job.
	Added more functionality to the 'Manage people' menu, where if you're in the Job or Permission management screen, a tab appears which allows you to quickly switch between slaves.
	Added copy & paste buttons to the Job Schedule, Job Settings, and Permissions sections of the slave management UI, allowing you to quickly copy & paste your settings between slaves.
	Added new 'Lube pills' permission under the 'Sex' permission category, which makes your slave stay on lube pills.
	Slaves will now consume pills via permission settings twice per day (at midday and midnight), which will be shown in the office's occupancy ledger, instead of having them invisibly applied at the end of every turn.

Other:
	Characters who are infertile (via the barren trait or menopause) will no longer gain the 'risk of pregnancy' status effect, nor will anyone who receives a creampie from a character with the 'sterile' trait.
	Elementals which are summoned by an NPC now have perks and spells automatically assigned to them based on their form (i.e. stone elementals will get earth spells/perks, fire elementals will get fire spells/perks, etc.).
	Slightly altered the randomised colours for imps' clothing and arcanist hats in Submission random encounters.
	When Yui equips clothing onto you as part of her demonstration scenes, you are now given the associated key to unlock them.
	The 'Human Spawn Rate' setting (in Content Options -> Furry Preferences) now affects the subspecies of spawned slimes (i.e if your Human Spawn Rate is set to 50%, half of all slimes will have human bodies, 100% and all slimes will have human bodies, etc.). 
	Changed the 'artist priority' setting from a single artist preference to a priority list of all artists, with default ordering based on the number of artworks each artist has in the game (and your preferred artist will be placed at the top when loading into this version).
	The clothing icons shown the encyclopedia are now displayed based on their appearance when equipped into the associated slot (e.g. the 'electrical tape' will show as two crosses when viewed in the 'nipple' slot section).
	During bad ends you can now open your inventory to view your clothing (but cannot manipulate it in any way).
	Added a minor variation to virginity loss text for when Sleip fucks you as a doll.
	Improved the racial icon for owl-morphs.
	
Bugs:
	Typo fixes and some minor scene improvements (Enforcer HQ corridor).
	Fixed issue where the doll bad end content would break if you'd previously gained 100 obedience during Murk's bad end content.
	Fixed bug where fetish-altering potions which were forced onto you (either after losing to an NPC in combat or after surrendering to them) would apply random fetish effects instead of the targeted ones which the NPC wanted (which was resulting in a never-ending process of fetishes being forced onto you after combat/surrender).
	NPCs who are forcing transformations on the player will no longer try to shrink or grow crotch-boobs if the player doesn't have crotch-boobs.
	Fixed bug where a character's default modifiers for milk, cum, and girlcum would always be restored when loading a game, even if they'd previously transformed them away.
	Fixed bug where Oglix's elemental, Golix, wouldn't be present during any of her scenes.
	In the fight vs Silence (which occurs if you defeat Shadow before defeating Silence), her elemental will no longer be duplicated.
	Fixed bug where resetting your body via the debug menu would unequip all of your piercings.
	Fixed bug where turning imps into slimes would make their minimum/maximum heights revert to standard values, allowing them to be transformed to normal heights and then reverted to flesh to make them into demons.
	When accessing a slave's job or permissions via the button within the main slave management UI, the job/permission screen will no longer start partially scrolled down.
	Fixed bug where most of Yui's scene where she locks the player in chastity was missing.
	Fixed bug in sex where NPCs would sometimes fail to remove their partner's clothing which was blocking access to the sex area they wanted to interact with.
	Fixed bug in sex scenes where clothing removals were meant to be restricted, where after changing position the clothing removal restrictions would be lost.
	Text for a character's ass and anus becoming lubricated in sex scenes will no longer be shown if your anal content setting is turned off.
	Fixed bug in the occupancy ledger, where filtering slave events by day would sometimes show events that didn't occur during that day (this isn't a retroactive fix, but newly-generated events going forwards will be placed under the correct day within the occupancy ledger).
	The 'Kiss cheek' action is now correctly disabled while immobilised (to bring it in line with the behaviour of other 'loving' actions).
	Fixed bug where offspring you enslaved and transformed into dolls would still be affected by incest, therefore
	Fixed bug where after befriending a randomly-generated NPC, and then enslaving them, they would always use the resisting pace in sex scenes no matter their affection towards you.
	After betraying an NPC, the 'Continue' action is now coloured red like the other removal ones to make it clear that they're about to be removed from the game.
	Fixed bug in Nyan's blowjob sex scene, where she could get stuck repeatedly using the 'perform blowjob' sex action, which would make it impossible to end the sex scene.
	When equipping a clothing item which doesn't get removed on equip (such as the new tape items), any hidden enchantments will now be revealed on the underlying item (e.g. the roll of tape) instead of only on the applied item (e.g. the tape in an inventory slot).
	The 'Calming suggestion' and 'Lustful suggestion' sex actions are no longer available if the target is sleeping.
	Fixed bug where the 'Arcane storm (protected)' status effect was only applying to interior locations within Dominion.
	You no longer earn Faire tickets from using the buyback menu with Fae & Siliva.
	Stopped background errors from being generated when mousing over an NPC's equipped clothing and weapons while in the buyback menu.
	Fixed several issues with Vronti's sex scenes: incorrect position slots when performing a handjob; being able to swap into slots which were meant to be blocked; the vaginal sex option not being available after performing anilingus.
	Fixed bug where if you tried equipping a clothing item which doesn't get removed on equip (such as the new tape items) into a blocked slot, the clothing would be duplicated.
	Fixed issue where Fae & Silvia's sex scenes would softlock and throw background errors.
	In the morning oral sex scene with Fae & Silvia (after they sleep over in your room), Silvia no longer starts the sex scene performing cunnilingus if your pussy is blocked.
	Fixed bug where tooltips would not work for clothing items in the encyclopedia if they were present in more than one section (e.g. the 'electrical tape' item being present within the 'anus' and 'vagina' sections).
	The bar upgrade in the spa is no longer missing a description in its information tooltip.
	Fixed bug in sex scenes in which clothing unequipping was meant to be disabled, where you were still able to 'Discard/Drop/Store' the clothing.
	The two tiles within 'The Creamy Bakey' map are now correctly treated as being indoors, and so characters within it are immune to weather effects.
	Fixed inventory rendering issues in light mode.
	Fixed issue where clothing that spawns with the sealing enchantment which costs 5 essences to remove wouldn't stack in the inventory with identical clothing which had had that enchantment removed and then re-added.
	Fixed bug where sometimes the main content would not scroll back up to the top when a new scene was presented to you.

---------------------

PATCH NOTES FOR v0.4.10.7

Contributors:
	Enhancement: Add sybaritic potion (refractory potion), which increases the drinker's desired orgasms by 3-5 when consumed during sex, otherwise provides 1-4 essences. (PR#1829 by CognitiveMist)
	Fixed a bug where a dildo would be treated like a real penis and cause clothing to get dirty when orgasming. (PR#1820 by alfadorfox)
	Filled in some missing parsing. (PR#1780 by MintyChip)
	
Engine/Modding:
	Moved the 'hyena' colour from the base res folder to the mod folder to conform with the location of the rest of the hyena-related files.
	
Gameplay:
	If you have bad ends turned off in your content settings, you will no longer encounter a bad end in the new side quest content.
	
Slaves:
	Slaves who have permission to clean themselves will now only do so if they're not at work, or at a work type which allows cleaning (the jobs which do not allow cleaning are 'test subject', 'statue', 'public fucktoy', and 'dairy cow').
	Added a new cleanliness permission, 'Remove Odours', which will make the slave remove musky odours when they wash themselves.
	
Sex:
	Added three new sadistic sex actions: 'Slap pussy', 'Pinch clit', and 'Slap cock'. (These actions are only available to characters with the 'sadist' fetish.)
	Virginity loss scenes now take into account whether your partner is asleep.
	When having sleep sex, you can no longer tell your partner to grow a cock, offer/request different areas, nor grant/revoke permissions.
	Added check for sleeping partner in the 'Deny' action.
	Added a new 'locked in stocks' immobilisation type, which is applied to the character being locked into stocks in all stocks-based sex scenes.
	Penetration-on-penetration ongoing sex actions (such as handjob reactions) are now available during immobilisation sex.
	Added more checks for a mute character in orgasm actions.
	Added description variation for resisting characters who request their partner to pull out.
	In the 'Orgasms' status effect tooltip, you can now see how many orgasms your character requires in sex to be satisfied. While this doesn't have an impact after sex, your consensual partners will want to satisfy you before ending sex, so the information is relevant for that.
	
Other:
	Properly centre-aligned the icons for the 'elemental striker' and 'elemental defender' perks and significantly increased their effects.
	When viewing the tooltip for interacting with a missing slave, it will now say if they're in a slave lounge instead of erroneously saying that they're out at work.
	Improved tooltip description for racial books.
	When you free the slaves in the stocks in Slaver Alley, a new group of slaves will appear after ~6 hours have passed, instead of at midnight.
	Ingesting fluids in the milking room now passes 5 minutes of time instead of 1 hour.

Bugs:
	Typo, parsing, and formatting fixes.
	Fixed issue where demons were being affected by menopause.
	If you have anal/foot/armpit content disabled, the associated fetish preferences are no longer displayed during character creation.
	Fixed bug where your character could sometimes end up with the 'sleeping' or 'heavily sleeping' status effects stuck on you after sleeping.
	Fixed bug where starting double penetration would first stop the other ongoing penis-vagina action, resulting in a simple swap of who was penetrating the vagina (and throwing some parsing errors) instead of resulting in a double penetration.
	The 'Spawn attacker' function of the debug menu now correctly spawns the NPC as the race stage you select, instead of always spawning them as the 'lesser' stage.
	You can no longer equip sex toys during Rose's domination scene (while you're locked in stocks).
	Fixed bug in slaves' job management, where the 'Office' job had all of its hourly spots grayed out when it reached capacity, unlike all other jobs which kept the slots visible.
	Fixed bug in feral sex scenes where NPCs could generate sex preferences that involved breasts or fingers even if the feral target had no breasts nor fingers.
	Fixed bug where all pierced areas would be reset when using the debug menu's 'race resets' or choosing to transform into a horse-girl for Sterope.
	Fixed bug where if a weapon had all 5 damage types available, then it would break the formatting when viewing the weapons page in the encyclopedia.
	If getting transformed into a doll as a demon, you no longer keep your wings/tail/horns.
	Fixed issue where when you leaded a saved game, all characters regained all of their default modifiers for all penetration and orifice types (penis, vagina, urethra, clit, anus, spinneret, nipples, crotch-nipples, mouth, tongue) instead of only the ones they had when the game was saved.
	After being transformed into a demon by Lyssieth, she will now be listed as your mother in her character details page, and in Elizabeth's details she will now be listed as your half-sister.
	Fixed minor issue with tooltip formatting for some items.

---------------------

PATCH NOTES FOR v0.4.10.6

Bugs:
	Fixed bug where interacting with any demonic taurs would often freeze the game.
	
---------------------

PATCH NOTES FOR v0.4.10.5

Contributors:
	Fixed an erroneous error message in the Util.getClosestStringMatch() function. (by AceXP)
	Improved error.log information to include build type. (by CognitiveMist)
	Improved Maven Compatibility Across JDK Versions. (PR#1745 by NoHornyOnMain)
	Fixed game crashing on leap days. (PR#1814 by Miigon)
	Cached compiled Javascript objects for improved performance (PR#1802 by tarbh-uisge) (Also thanks to CognitiveMist for PR#1442 which implemented the bulk of the original code which this PR uses.)
	Documentation: Specify svgo version compatible with svgoConfig.yml (PR#1813 by CognitiveMist)
	Implemented a few minor bug fixes (which could cause background errors or softlocks). (PR#1821 by CognitiveMist)
	Sanitized quicksave file name to prevent loading issues when playing as a character whose name contains a space or period. (PR#1781 by SightglassCat)
	Enhancement: Store minimap zoom level in the game properties (so your zoom level will be remembered when restarting the game). (PR#1832 by CognitiveMist)
	Added 'Chinese characters tally' as new tattoo counter type. (PR#1805 by CKRainbow)
	Bugfix: pressing enter when naming enchant or tattoo undoes the last character. (PR#1834 by CognitiveMist)

Engine/Modding:
	Improved the debug menu's 'Spawn attacker' action so that you can choose the gender of the spawned attacker.
	When debug mode is turned on, the time it takes to end each turn is displayed in the title of the window.
	Added 'DUPLICATE_WHEN_EQUIP' as an ItemTag, which is used for the new electrical tape clothing item.
	Added 'countDuplicates' attribute to the 'numberRequiredForCompleteSet' value in SetBonus files, allowing you to define whether or not you want duplicates of clothing or weapon types to count towards the required number of items to activate the set bonus. (See 'res/mods/innoxia/setBonuses/template.xml' for more info.)

Clothing:
	Added 'square nipple rings' (androgynous, nipple piercing slot, sold by Kate).
	Added 'electrical tape' (androgynous, mouth/nipple/vagina/anus slots, sold by Ralph).
	Removed 'tape crosses' as they're now a part of the new 'electrical tape' clothing item. Any existing 'tape crosses' in your save file will be converted into 'electrical tape' when loading into this version.
	Added 'duct tape' (androgynous, wrist/ankle/mouth slots, sold by Ralph).
	Added more recolouring options to the sun and snowflake themed accessories.

Slaves:
	Added 4 new job permissions to the prostitute job, allowing your slaves to act as dominant partners while working as a prostitute.
	When working as a prostitute, slaves can now perform cunnilingus as well as blowjobs when the oral permission is activated.
	Improved the formatting of prostitute events in the occupancy manager.
	Prostitute and public fucktoy slaves will no longer engage in anal sex if your anal content setting is disabled.
	Job settings for slaves now respect your content options (e.g. if you have anal content turned off, you won't see the 'Allow anal' setting for the prostitute or public fucktoy jobs.)
	If your slaves are given the 'Silence' permission, they are now treated as though they're mute, and cannot speak during sex. (They will continue to talk during non-sex interactions as I still need to add mute behaviour for most slave scenes...)
	When interacting with one of your owned dolls, if either you or the doll has a D.E.C.K. in your inventories, then you can now use the 'Transformations' action instead of accessing the inventory and manually using the D.E.C.K. on them.
	
Sex:
	Further improved the 'Grow cock' sex action, so if a character has a penis, and then that penis is removed, the 'Grow cock' action in sex will restore that character's previous penis instead of generating a generic new one for them.
	The 'Grow cock' action when performed on a partner is now no longer available if your partner is resisting.

Other:
	When in a feral form, you can no longer get pregnant (this is a temporary change to fix some issues with Sterope's content, but I will soon re-enable feral pregnancies and fix her content properly).
	The DECK can now transform dolls' wings, horns, antennae, and tails.
	Split the item view in the encyclopedia into three separate screens to make navigation a little easier.
	NPCs with the bondage applier fetish will no longer spawn with enslavement clothing in their inventory (such as the metal collar), as they are not able to enslave others.
	Character height is now limited to 200cm during character creation, and the UI for height selection has been slightly improved.
	Updated the starting jewellery for piercing slots in the character creation based on femininity.
	Increased Rose's starting age from 18 to 20 (as I felt like she'd need more time to build up her relationship with Lilaya).
	Oglix now has the tribal tattoo and scars which are shown in her artwork.
	Submissive NPCs at the Watering Hole who have the 'unwilling fuck-toy' fetish will now engage in rape-play in the toilets.
	Added a small dialogue variation to the scene with Hammer & Ghost just before the raid, where if you ask them about their weapons while carrying an HLF weapon yourself, Hammer will comment on it.
	You can now take the 'vaginal virginity' fetish during character creation even if you set vaginal sex experience to a non-zero value, allowing you to start the game with the 'broken virgin' debuff if you want to.
	Rabbit and reindeer balls are now covered in their associated fur instead of sharing the same characteristics (such as colour) with their penis.
	Slightly improved the 'Glacial' and 'Radiant' status effect icons.
	In Dominion, the generic population in the 'Characters present' window now changes at night.
	When changing femininity during character creation, your character's body will slightly adjust to reflect these changes (penis and breast sizes are affected, but can always be changed in the following customisation menus).
	When NPCs engage in generic sex (such as when working as a prostitute or as a slave in the stocks), each instance of this sex will be counted as a unique partner for the purposes of tattoo counters.

Bugs:
	Typo and parsing fixes.
	Fixed issue where you were unable to buy a DECK from Saellatrix, even if you had enough money to do so.
	Prevented game logic parsing commands from executing when typed into an item's name field in the enchantment menu.
	Fixed bug where anthro dolls would never spawn with wings, horns, antennae, or tails.
	Fixed issue where you couldn't interact with dolls who were stationed on staircase tiles.
	Interest on your savings is now correctly calculated for the flames which you store in the bank at Elis.
	Fixed incorrect description in the 'Heavily pregnant' status effect update, where it would only recognise that you lay eggs if you had a harpy vagina, instead of any egg-laying vagina.
	Fixed page title during character creation's tattoo addition showing an incorrect location name.
	NPCs will no longer spawn with birthdays in the future.
	Fixed bug where using the alarm to sleep would not work if the current time was either the same as your alarm's time, or 1 minute past the alarm's time. (Fixed in all locations where you can use your alarm: in your room at Lilaya's mansion, in your room at The Red Dragon, or at Evelyx's dairy.)
	Fixed bug where you'd get to know what Hammer & Ghost looked like naked when they changed into their civilian and fully-geared-up outfits, even though they didn't strip naked.
	You can now transform breast rows in the self-TF menu if your multi-breast settings are set to anything other than 'Disabled', as the setting tooltips imply.
	Fixed issue where body content preferences were not taken into account in a few places (which was affecting skin colour, breast rows, and crotch boobs).
	Fixed bug where the 'Bar' action in The Crossed Blades would always be available, even if you'd already introduced yourself to Golix.
	Using the 'Quick sex' action now correctly results in a character cumming on their partner's breasts if they are engaged in paizuri (or any penis on non-penetrable orifice) for the main sex preference.
	Fixed bug where items of clothing could be mentioned multiple times when being described as being cummed on at the end of quick sex.
	Fixed bug where time was inadvertently passing when selecting options in Helena's slave customisation menu.
	Using a condom while trading with an NPC will no longer softlock the scene and duplicate the condom.
	Fixed issue where using a used condom and then backing out before choosing an orifice would make the condom disappear from your inventory until the scene changed.
	Fixed bug where creampie actions could sometimes result in all sex participants cumming into the targeted character regardless of whether or not they were penetrating them or even if they had a penis (this bug was always encountered when using autofellatio and deepthroating yourself when spectating an ongoing sex scene).
	When in hiding while spectating a sex scene, you can no longer manipulate the participants' clothes or give them items.
	Added missing generic 'shoppers' population for Nyan's store tile (only present when not in storeroom with Nyan).
	Fixed cow ears being described as being high up on your head (as through they were pointed ears like a fox's).
	The generic 'trader' occupation is no longer available as a job suggestion to friendly occupants.
	Fixed bug where random NPCs would never spawn as half-demon taurs, no matter what you'd set your half-demon and taur preferences to be.
	Fixed bug where half-demon taurs would always have their genitals referred to as being those of a 'demonic-horse', instead of a 'demonic-LEG_RACE'.
	Fixed bug where slimes would always spawn as 'human' slimes, instead of representing your subspecies preferences. (i.e. Slimes will now spawn with a body drawn from the full range of subspecies that are enabled in your content settings.)
	When squirting during orgasm, the text now correctly describes the orgasming character as the one whose clothing is being dirtied (instead of a random NPC).
	Fixed multiple parsing errors being displayed when receiving oral sex from Nyan & Leotie.
	In Nyan & Leotie oral threesome, when blowjob or cunnilingus is somehow ended, and they aren't involved in an ongoing oral action, they will now restart the blowjob/cunnilingus.
	In sex, when a character joins in on an ongoing action (double-blowjob, double-cunnilingus, double-penetration), then any other ongoing actions using the associated sex areas are now correctly stopped. (e.g. Nipple kissing into double blowjob would not stop the ongoing nipple kissing.)
	Fixed bug in sex where starting an ongoing action involving the MOUTH area would not stop any ongoing TONGUE actions, and vice versa.
	Fixed bug where using an enslavement item on an NPC who wasn't able to be enslaved would still add them as your slave and teleport them to slaver alley (this bug was present for the two imps who guard each of the fortresses in Submission).
	Fixed issue where the 'Furry tail penetrations' content setting would only allow furry tails to be used in sex if they were prehensile, instead of following the same rules as non-furry tails (which is if they're prehensile OR if they're longer than 50% of the character's height).
	When bidding on a slave at the auction block in slaver alley, the correct opening scene is now displayed, instead of the generic import information text.
	Sex area tooltips will no longer state that non-penis penetrations are swollen due to a knot during the turn when an orgasming character is knotting an orifice.
	Fixed bug where when a character knotted their partner (which requires them to insert their penis as deep as possible) all other ongoing penetrations would also be inserted as deep as possible, even if the orgasming character wouldn't ordinarily want to do that.
	When leaving the Centaur Carriage Depot, only 2 minutes now pass instead of an hour.
	A character now needs both a katana and a wakizashi to complete the 'daisho' set bonus. Wielding two katanas or two wakizashis will no longer work.
	Fixed bug in the doll side quest, where if you're a doll, you were able to reset the perk tree and buy perks, and were therefore able to obtain all of the perks which were meant to be disabled during that quest.
	Fixed bug where after learning a spell upgrade, you could continue to click on the owned upgrade which would keep on deducting your spell points.
	When meeting Fia before starting the main part of the doll quest, the characters present window no longer lists a large nubmer of generic characters as being present.
	Fixed bug where no subspecies were added to the 'storm immune' subspecies list, which resulted in there being no generic characters present during an arcane storm even though demons were described as being in the area.
	Fixed bug in the new side quest's bad end where both your and Fiammetta's serial numbers would be identical.
	Fixed issue with Vronti's blowjob and handjob sex scenes where both of you would start in incorrect positions and background errors would be thrown.
	Feet and toes for characters with tails instead of legs are now correctly referred to as tails/tips instead of feet/toes.
	Added missing 'porcelain' skin colour to the possible varieties which characters can spawn with.
	When starting a new game, your character is no longer influenced by your penis and breast size preferences, so as to keep the starting values for penis and breast sizes within the intended range.
	Fixed bug where trying to get Kate to modify a tattoo which didn't have any writing nor a counter would not work and throw background errors.

---------------------

PATCH NOTES FOR v0.4.10.3

Davyn's Artwork (https://twitter.com/davyndraw):
	Added artwork for Wes, including variations for if he's enslaved.
	Added artwork for Elle, including variations for if she's enslaved.

Engine/Modding:
	Added a new addEffect() method to AbstractClothing, allowing you to add effects to clothing within the parser.
	Added parser hooks for TFModifier ('ENCHANTMENT_MODIFIER_' prefix) and TFPotency ('ENCHANTMENT_POTENCY_' prefix) so that you can use the new addEffect() method.
	Fixed bug where if 'orgasmCumTargets' variable was used in custom sex managers, if the sex scene was initialised it would soft-lock when trying to initialise in repeated scenes.
	Fixed issue where the 'orgasmEncourageBehaviours' variable in custom sex managers wouldn't work if you were trying to define how the performing character should react if they were also the one being penetrated.
	The 'preferredTarget' attribute in sex manager files now works for the player character by setting that defined character as the one that's targeted by the player at the start of sex (but has no effect after that).

Gameplay:
	Added a new side quest involving Saellatrix and her shop, 'Lovienne's Luxuries'. This quest can be started after obtaining the 'Angelixx's Diary' item in Elis during the main quest by talking to the SWORD Enforcers in Elis. This quest contains a bad end.
	The player's hair now grows at a rate of 1cm per week, which can be changed to 1cm per day or per hour, or disabled entirely, via the setting in 'Content Options', 'Bodies', 'Hair Growth'.
	Added a small amount of content to Dale which ends with making him a heavy sleeper and being able to have sleep sex with him. (Talk to him about his work to see the new dialogue option appear.)
	Added an option to receive a footjob while performing cunnilingus on Vanessa/Ms. Cunningham.

Clothing & Items:
	Added 'equine dildo' (androgynous, Vagina/Anus/Mouth slots, sold by Saellatrix, flared dildo with 54cm length and 'average' girth, five stickers to choose colour variations).
	Added 'polo shirt' (masculine, torso slot, sold by Nyan).
	Added 'chinos' (masculine, leg slot, sold by Nyan).
	Added 'desaturated pink' and 'dark desaturated pink' colours for clothing.
	Added 'dull' variations of all colours for clothing/weapons/tattoos.
	The 'D.E.C.K.' item is now able to be sold.
	Added more colours to the 'spiked collar' clothing item.
	The 'chemise' is now correctly tagged as being transparent, as its description implies.

Tattoos:
	Added several new counter types related to orifice penetrations.
	The option for anal and nipple-penetration tattoo counters are now correctly hidden when the associated content toggle is turned off.
	You can now choose to start a tattoo's counter at 0, or instead choose the previous behaviour of starting with the counter showing all previous experiences.

Slave management:
	Added a 'Rapist' permission for slaves (if non-con is off then this permission is hidden, and the game will act as though it is disabled for all slaves).
	Slaves will now only rape other slaves if they have the rapist permission, do not have a negative desire towards the non-con fetish, and do not like their target or the target has a positive desire towards the non-con victim fetish.
	Slaves who have the 'Use You' permission will now only rape the player under the same set of circumstances as those listed above, otherwise the player is now able to turn down a slave who approaches them for sex.
	Slaves can now ambush you for sex in the corridor tiles in Lilaya's dungeon.

Sex:
	Using quick sex now correctly applies cumming effects if interactions don't involve an orifice.
	Quick sex now takes into account cum target preferences that are defined in the sex manager, and also applies additional slot dirtying for if the cumming character produces a lot of cum.
	Characters standing beside one another in the 'against wall' position can now interact with one another via kissing and using full appendage interactions.
	Maximum arousal gain per sex turn is now limited to 15, so sex should last a little longer (will be most noticeable in group sex, where the maximum arousal per turn was previously getting quite high and making sex end very quickly).
	Dominant NPCs who don't have the 'giving oral' fetish are now less likely to perform oral on their submissive partners.
	Using the 'Grow cock (self)' action during sex no longer resets your penis modifiers to their default values.

Other:
	Generic naming for clothing based on enchantments (i.e. the 'of X' postfixes) now prioritise the positive attribute if a negative and positive attribute have the same magnitude.
	Doll orifices now have access to 'flesh' colour as a secondary colour.
	Characters can now be marked by up to five characters' musk at once (instead of just 1).
	Removed the 'All' and 'All clothing' actions in the debug menu's item viewer (as there were too many items to display in one scene) and added a clothing femininity filter action.
	Renamed the 'BDSM' status effect to 'Bound Bitch'.
	Added options to pass time until the next sunrise and next sunset in the loiter menu.
	Added a bar to the UI beneath the current time to give a visual depiction of daylight hours.
	Added dialogue variations for mute slaves in the player-slave and slave-slave random sexual encounters.
	Added 'side-parted' as a hairstyle.
	Ferals with a leg configuration that has 'large genitals' (quadrupeds, arachnids, and avians) will now have larger penises (e.g. feral horses now have ~44cm penises by default instead of the previous ~22cm).
	Reading 'Arcane Arousal' in Lilaya's library no longer increments your 'spell efficiency' attribute by 1 (this was the only place in the entire game where a non-corruption attribute could be increased and so it felt out of place).
	Added a new book to Lilaya's library about the history of ferals.

Sterope's tavern content fixes:
	Improved dialogue flow, fixed some parsing, and improved some tooltip and action text.
	The first time you meet Sterope in the tavern, a random centaur now always spawns (to more clearly display what kind of content should be expected in her scenes).
	Both dominant and submissive feral sex content is unlocked after convincing Sterope to stay as a greater horse-girl (which can now be done in both post-submissive and post-dominant sex).
	Fixed player's clothing disappearing when transforming.
	Fixed player's feral clothing remaining equipped after feral sex.
	Sterope has her addictions, hypnosis effects, and musk marking removed after her sex scenes have finished (so her scenes at work aren't affected).
	Fixed issue where Sterope would sometimes revert to her partial furry form, even if you'd told her to remain as a greater horse-girl.
	When transforming into a dominant feral, you now grow a penis with which to fuck Sterope.
	
Bugs:
	Parsing and typo fixes.
	Dolls can no longer gain fetishes from clothing or tattoos.
	Fixed harpy skin colours using clothing colours instead of covering colours.
	Fixed issue in modded sex managers where sex actions defined within a character's 'uniqueSexActions' element would sometimes be available for all characters in the sex scene, instead of just for the character who has the action within their 'uniqueSexActions' element.
	Fixed bug where immobilisation descriptions for all immobilisation types would be displayed one after the other if immobilised during your partner's body part reveals in sex.
	Dolls can no longer gain the 'Risk of pregnancy' status effect.
	Fixed bug where changes to a character's inventory would affect copies located in Game.savedInventories (which could potentially have been causing bugs in content related to the bank, Murk, and Scarlett).
	Fixed newly created anthropomorphic dolls always having human legs instead of the expected anthropomorphic racial type.
	Fixed bug where at the start of sex scenes, the dialogue would sometimes start partially scrolled down.
	Fluid recolouring now uses an accurate list of fluid colour values instead of the same one that's used for hair & fur.
	Kalahari's tube top is now black, as it's shown in her artwork.
	Fixed minor bug in Nyan's romance quest, where after defeating Wolfgang & Karl in combat, they would disappear before choosing to let them leave.
	Fixed the subspecies requirement for some actions listing an incorrect subspecies (mainly displaying 'half-demon' instead of 'demon').
	In Dale's under-desk blowjob scene, Dale will now restart the blowjob if he pulls out when orgasming.
	You can now stop Dale's blowjob sex scene.
	When choosing to be 'Mated' when working as a cow in Evelyx's Dairy, the NPC will now always creampie you if you aren't visibly pregnant and they're fucking your pussy.
	Fixed issue where you could request a creampie or pullout from a sleeping character.

---------------------

PATCH NOTES FOR v0.4.10

FriendlyAlienFriend's Artwork (https://twitter.com/thealienfriend):
	Added Lunexis artwork (with pregnant and crotch-boob variations).

Pusspuss's Artwork (https://twitter.com/PusspussARTZ):
	Added Yui artwork (with pregnant variations).

Engine/Modding:
	Added support for multiple 'startingImmobilisation' elements per character in modded sex managers.
	In modded combat moves, you can now use 'UNARMED' as a damage type to automatically use the correct damage type based on the attacker's body.
	Added a new 'Outfit' action to the debug menu's 'Item view' tab, allowing you to apply any outfit to a generic doll for testing purposes.
	Added a new 'Combat moves' action to the debug menu's 'Misc.' tab, allowing you to see all combat moves and their IDs.
	Added 'KNOT' as a new OrgasmBehaviour (for use in modded sex managers).
	Added hook for OrificeDepth enum to parsing engine, with 'ORIFICE_DEPTH_' prefixes.

Gameplay:
	The map for 'Lovienne's Luxuries' needed to be regenerated as part of this update, so it will have been reset to be as though you haven't explored it yet.

Images:
	Increased the size of the artwork images shown in characters' body overview tooltip.
	Added several new keywords for image file names to help filter images when in-game (keywords and their behaviour can be seen in res/images/characters/modding.txt).

Clothing:
	Added 'muzzle' (androgynous, BDSM set, mouth slot, blocks mouth, sold by Saellatrix).
	Added 'bar gag' (androgynous, BDSM set, mouth slot, blocks mouth, sold by Saellatrix).
	Updated the 'strapless bodysuit' to use the same blocking logic as 'lowback bodysuit', which should fix some issues with NPCs struggling to displace it (such as when combined with pantyhose).
	The 'Thin bangles' and 'Bangle' can now be worn in the tail slot as well as the wrist slot.
	The 'Bangle' is now androgynous instead of feminine.
	The 'strapless strap-on' now has a base rarity of 'common' instead of 'epic'.
	Added an 'Inserts' sticker option to the 'bunny headband' (thanks to DSG).
	Swapped the primary and secondary colours for the 'heart-shaped barbells' clothing (this will automatically be applied to your old barbells so you don't need to manually fix them when loading into this version).
	Added stickers to the 'breeder collar' to enable you to set the text to 'breeder' (default), 'bimbo', 'bitch', 'slut', 'cum slut', or 'whore', and changed the name to 'ornate collar'.

Items:
	Saellatrix now sells Silic Oil (this was previously unobtainable unless spawned via debug menu). 
	Changed colour of the rejuvenation potion to be light blue.

Mystery Kink rework:
	'Mystery Kink' is now called 'Succubus's Kiss', and has a new icon.
	Instead of adding/removing a random fetish, 'Succubus's Kiss' now gives +50 lust (and +50 arousal during sex).
	It retains its old enchantment mechanics (to create fetish potions), and can now also be enchanted with an empty primary and secondary modifier to give it the same 'adding/removing a random fetish' which Mystery Kink used to have by default.

Combat:
	Many special combat moves which previously did physical damage, or were incorrectly applying 'unarmed' damage, are now correctly using the appropriate damage type based on the attacker's body type or whether they're under the effects of cloak of flames.
	The 'scratch' and 'squirrel scratch' special attacks now critically hit when the defender has no shielding.

Sex:
	Added tail-to-nipple, tail-to-crotch-nipple, tentacle-to-nipple, and tentacle-to-crotch-nipple sex actions, allowing you to penetrate fuckable nipples with tails and tentacles.
	Characters will no longer desire to perform tail-to-breast or tentacle-to-breast sex types during sex, as those sex types are now covered instead by the newly added tail/tentacle actions.
	Characters will no longer perform deep penetrations on sleeping size queens or masochists.
	Added support for characters to be immobilised in multiple ways during sex (for example, sleeping slaves in a cell with chains will now start sex being both asleep and chained up).
	Sleeping characters no longer lose affection towards partners at the end of sex due to non-con or failure to satisfy.

Other:
	The 'bonding' slave interaction event will no longer occur between two dolls (as it doesn't make sense for dolls to attempt to bond with one another).
	The 'News' action at Dominion's central plaza now randomly shows each news variation once before being disabled (and is enabled again when leaving and re-entering the tile).
	Lunexis now has two pairs of breasts instead of three.
	Changed the colour and name of the default orifice-interior colour from 'fleshy-pink' to 'flesh'.
	When debug mode is enabled, dying clothing and dying/reforging weapons no longer requires dye brushes or reforge hammers.
	Renamed a few slave jobs to better reflect the job that the slave is performing (such as 'bedroom' -> 'bedroom servant').
	Imp fortresses no longer undergo a complete reset after you've defeated them all plus Meraxis. Instead, they will return to their fortress ~5 days after defeating Meraxis, but their surrounding tunnels will remain pacified. This is retroactively applied when loading into this version.
	Removed pink and dark pink from pig-morphs' natural fur colours, as they seemed to be too pink to be believable as a natural colour.
	Made it slightly more obvious when a character is bald in the overview appearance tooltip (when hovering over a character's race icon by their name).
	Slightly improved tooltip UI for clothing with fetish effects.
	NPCs' relationships with other NPCs will now be displayed in their character information screen, provided that you have met the other NPC.

Bugs:
	Parsing and typo fixes.
	Fixed bug where guests in the mansion would always stay in their room, even if they had a job.
	If you have an item of clothing which provides vaginal or vaginal urethra cum retention, then creampies in those orifices will be reduced to the maximum of 250mL when becoming pregnant, instead of being expelled entirely.
	Fixed several incorrect descriptions during sex related to sleeping characters.
	Fixed incorrect descriptions for when encouraging creampie/knot/pullout for self-penetrating characters.
	When setting a slave free, their assigned hourly slave jobs are now reset to IDLE (and when loading into this version, guests who have an incompatible slave job assigned to an hour slot will have that job reset to IDLE).
	Fixed issue where using a used condom on an NPC while not in sex would either not work or possibly soft-lock the game.
	Fixed bug where a character's girlcum was being treated as musky only if their cum was musky, instead of whether or not their girlcum had the 'musky' fluid modifier.
	Bimbo sentence parsing no longer inserts bimbo additions around noises denoted by '~' (e.g. ~Mmm!~).
	Fixed background errors being thrown due to missing 'sexBlockedReason' elements in worldType files.
	Fixed issue where the 'pugilist', 'elder lilin's helper', and 'sex doll' jobs were available for guests in the mansion.
	Random NPCs will no longer be sleeping during their encounters with you, nor will your elementals sometimes be asleep.
	Fixed issue where it was possible to have no actions available, causing you to get stuck, in Eisek's 'Confront the mob' scene.
	Damage calculations in combat now correctly take into account the attacker's unarmed damage type.
	Fixed the 'scold' greeting for offspring having the prostitute scene trigger for mugger offspring and vice versa.
	Fixed issue where Submission attackers could spawn with the prostitute occupation, instead of all being muggers as intended.
	Unlocking doll closets before obtaining a slaver license or permission to house friendly occupants now correctly grants you access to room management menus in Lilaya's mansion.
	Fixed bug where 'Anthro Special' dolls would always spawn with no tail, even if their species should have a tail.
	Fixed bug where if you chose to buy an 'Anthro Special' doll and proceeded to select a subspecies, then switched back to the DD or HH option, the purchased doll would be of the subspecies you originally selected instead of a default human.
	Removed races which were incompatible with doll bodies from the list when purchasing an anthro doll from Saellatrix (e.g. snow-leopards require fluffy fur, which is unavailable for dolls).
	Clothing enchanted with the 'cum retention' behaviour now correctly has the generic name postfix of 'plugging' instead of 'transformation'.
	Fixed issue where clothing with the same colour patterns would sometimes not stack with one another, which was due to one or more hidden pattern colours being different.
	Fixed bug where you couldn't rehouse purchased dolls, even if the targeted room had a doll closet upgrade.
	Fixed bug where the action to enter Dominion Express was duplicated when it was meant to be disabled, allowing you to enter the building during closing hours.
	Doll sex events no longer describe a risk of pregnancy (as dolls cannot be impregnated).
	Penile and vaginal urethra status effects during sex will no longer be displayed if the character does not have a penis or vagina, respectively.
	Fixed bug where you could transform an imp into a demon by shrinking them below the minimum height value when transforming their leg configuration from quadrupedal to bipedal.
	When starting a new game, your aura will no longer be stuck at 0 until you sleep.
	When starting a new game, your core health and arcane values will now be correctly set to 1.
	Sleeping characters and immobile dolls will no longer use items during sex scenes.
	When a character is switched from a normal sex slot to a spectator slot, all ongoing actions involving that character are now correctly stopped.
	Hannah will now correctly turn up to work at the gym at 08:00 without needing you to exit and re-enter the gym first.
	Fixed issue where cumming on an armpit or marking it with heavy lipstick would cum on/mark the target's legs instead of their torso.
	Fixed bug where you could get prizes from Moreno in Elis's Farmer's Market even if you had no faire tickets, and also a bug where the metal and wooden bat prizes would not actually give you a bat.
	Random NPCs in the club will no longer spawn wearing a balaclava.
	Fixed a few background errors being thrown when generating some clothing outfits.
	Lunexis now has the correct surname to indicate she's a direct daughter of Lunette.
	Fixed issue where a character could be identified as an aunt/uncle to their own child (even if the child was a result of sibling incest, having the parents tagged as aunts/uncles seemed unnecessary).
	Fixed bug where the dialogue would sometimes be partially scrolled down when starting a sex scene.
	Fixed issue with Sleip and Nir having some incorrect covering colours.
	
---------------------

PATCH NOTES FOR v0.4.9.9

Tattoos:
	Added a 'Save/Load' dialogue when customising tattoos, allowing you to save your tattoo presets and then quickly load them into other slots or onto other characters.
	Tattoos can now be enchanted with 'creampie retention' in the same manner as clothing, and enchanted clothing or tattoos with a creampie retention enchantment now have the generic name postfix of 'of plugging' instead of 'of transformation'.
	Added a 'Modify' button to the tattoo addition screen, allowing you to modify your current tattoos instead of having to remove and then add new ones.
	The 'written out' tattoo counter style is now capitalised.
	Improved the images for 'Horse-shoe' and 'Lines' tattoos, renamed 'Paw' tattoo to 'Dog paw' and improved the image, and added 'Detailed flowers' and 'Cat paw' tattoos.
	
Other:
	Kate's womb tattoo now tracks current litter size, and she has some minor dialogue related to this when the player reacts to her pregnancy for the first time.
	The 'D.E.C.K' item is now classed as a unique item, and after purchasing one from Saellatrix, you are unable to purchase any more. If you have more than one D.E.C.K., extras will be removed when loading into this version and the cost will be refunded.
	The 'Nymphomaniac' perk now causes the owner to gain the 'Pent-up' and 'Chastity' status effects twice as quickly as normal.

Bugs:
	Characters who have a negative desire towards the pregnancy or cum addict fetishes will no longer use the 'Finger insemination' sex actions (so Lilaya will no longer use this action and then get mad at you for impregnating her).
	When buying a doll, Saellatrix now correctly says that your doll will be wearing a maid uniform instead of cat lingerie when confirming your choices.
	Fixed bug where Vicky would often repeatedly react to her and the player's pregnancy as though she was seeing it for the first time.
	Fixed incorrect tooltip descriptions and sizing for the 'Add/Remove' buttons in the tattoo management menu.
	The tooltip for the active item in the enchantment load/save screen now works.
	Reduced the chance for demons to have male offspring from 75% to 10%.
	Fixed NPC transformative potion generation setting ass size instead of hip size.
	Fixed issue where multiple characters with the 'object of desire' trait would all increase the orgasms required before satisfied, instead of this effect only being applied once as intended.
	Fixed issue where arm wings were described in a character's body description as being large enough to allow flight when they actually weren't.
	
---------------------

PATCH NOTES FOR v0.4.9.8

Engine/Modding:
	Minor improvements to Body.java class xml save formatting.
	Added copy constructors to all body part classes.

Gameplay:
	If the 'non-con' and 'rape-play allowed by default' content settings are enabled, then random NPCs with the unwilling fuck toy fetish will have 'rape-play' sex actions after defeating them in combat instead of the normal 'sex' ones.

Items:
	You can now use the arcane makeup set in sex.
	Added a new 'creampie retention' enchantment for clothing, which when used in combination with an orifice modifier, prevents creampies from being lost over time in the associated orifice.

Sex:
	Mute NPCs will no longer act as though they're trying to talk when reacting to the possible loss of their orifices' virginity.
	Orgasming characters will now only say the 'get pregnant' lines when giving their partner a creampie if their 'impregnation' fetish desire is positive, their partner is fertile, and the orgasming character is virile.
	Re-added 'Finger insemination' action which was temporarily removed from Brax's old sex content some time in v0.2.x. The action is now split into 4, which take the form of: partner-start-fingering, partner-ongoing-fingering, self-start-fingering, and self-ongoing-fingering.
	Added tracking of cum on body parts during sex, which can be seen in the inventory slot tooltips, and which is used to determine the availability and effects of the re-added 'Finger insemination' sex actions.

Combat:
	'Feral bite' now critically hits when the target has less than 25% health remaining.

Other:
	Added a 'Lip lisps' content setting, allowing you to enable or disable the lisp effect gained from having huge lips. (Accessed via 'Content options' -> 'Bodies' -> 'Lip lisps', being enabled by default.)
	Several very minor improvements to UI (transformation menu modifiers buttons, transparent covering icon, piercing inventory tooltips).
	Renamed 'clear' body covering to 'transparent' to make it a little more obvious what the covering was meant to represent.
	Dolls now correctly have doll-specific fluids (milk, cum, girlcum), which all start with 'slimy' and 'mineral oil' fluid modifiers. Doll fluids are worth 1/4 that of normal fluids.
	When a creampie dirties clothing that's covering the creampied orifice, the game is no longer interrupted by a message telling you that that's just happened, and instead a 'Creampie' event is added to the event log (in the bottom-right of the UI).
	Increased the true age of several unique demon characters (Amber, Kate, Natalya, Zaranix, and Lunexis), although their 'age appearance' remains unaffected.

Bugs:
	Parsing fixes.
	Fixed rare issue where the game would sometimes freeze and crash when an orgasm action caused body parts to get covered in cum.
	Fixed bug where the covering of taurs' asses and hips was linked to their torso covering instead of their leg covering.
	Fixed bug where unique NPCs who are your slaves (i.e. Scarlett and Brax) would never go to sleep.
	The 'barren' and 'firing blanks' perks now correctly stop applying their anti-pregnancy/impregnation effects when removed from your active trait bar.
	Additional speech patterns (such as those in bimbo speech) are no longer applied at the start of sentences. (So weird sentences such as 'Hello., um, I'm a bimbo!' will no longer appear.)
	The gender of offspring is no longer determined solely by gender preferences, and instead now correctly takes into account the 'chanceForMaleOffspring' value from the mother's race.
	Fixed bug where demonic offspring were unaffected by genetics.
	Fixed bug with stored cum (in the milking room and in orifices), where if the cum provider was transformed, their transformation would be reflected in their stored cum. (i.e. A character's stored cum now correctly saves their genetics at the moment of storage.)
	Fixed bug where if you attacked random characters who you've befriended in Elis's alleyways, you'd be presented with a scene which had no actions, preventing you from progressing.
	Made some very minor dialogue improvements to random NPC post-combat dialogue and corrected some minor inconsistencies in some of the scenes.
	Using the debug menu in sex will now correctly return you to the sex scene when exiting from it, instead of putting you in the default dialogue and thereby breaking the game.
	
---------------------

PATCH NOTES FOR v0.4.9.5

Engine/Modding:
	Added parser hooks for slave jobs and slave job settings, prefaced SLAVE_JOB_ and SLAVE_JOB_SETTING_.
	Added an optional 'doesNotAge' value to subspecies files to set whether or not members of that subspecies have their age appearance increment as normal.

Gameplay:
	Added more dialogue to Saellatrix (the succubus in the new sex toy shop).
	Finished implementing doll race mechanics, more details below.
	Added support for 'sleep sex', allowing you to engage in sleep sex with your sleeping slaves or friendly occupants. Your sleeping partner requires the new 'heavy sleeper' perk to be an active trait in order to have sex with them in their sleep.
	Added 'heavy sleeper' perk, as mentioned above, which enables sleep sex and also applies a 10x health and aura regeneration rate. (This addition did not require perk trees to be reset, so all characters' perks are unaffected when loading into this version.)
	Added sleep sex content for Kate (the succubus in 'Succubi's Secrets' in Dominion's shopping arcade).
	If the player has the 'heavy sleeper' trait active, then slave sex when sleeping in your room will now take place as sleep sex instead of being woken for sex by horny slaves. (Slaves require the 'Use you' permission and to be assigned to your room in order to be involved in this scene.)

Dolls:
	You can now purchase dolls from Saellatrix, with several options available to customise the doll when purchasing it.
	Removed some references implying dolls could get pregnant/impregnate others.
	Dolls will no longer spawn with special perks (such as 'dirty minded', 'health fanatic', etc.).
	Dolls no longer suffer from chastity status effects.
	You now correctly receive no essences post-sex from dolls' orgasms.
	Dolls' perk trees are no longer described as being a work-in-progress.

Sex:
	Added a new content option for setting how often you want to see full descriptions of revealed body parts during sex. (Accessed via 'Content options' -> 'Sex & Fetishes' -> 'Full exposure descriptions', with 'Always' as the default setting.)
	Minor improvements to some sex action text.
	Immobilised characters can no longer displace or remove clothing.

Other:
	Added dalmatian subspecies for dog-morphs (to be a dalmatian, be a dog-morph with floppy ears and white fur with black spots).
	Added 'femininity' and 'race' as sorting options for the slave management dialogue.
	The shady dealer will no longer sell Biojuice canisters before you've completed the slime queen side quest (to avoid an issue where the quest would not be available if you were already a slime before encountering a slime in Submission for the first time).
	The 'waiter/waitress' slave job now has a 0.5 hourly obedience increment (up from 0) to bring it in line with similar jobs.
	Demons, slimes, youko, elementals, and dolls no longer have their age appearance increment with the passage of time.

Bugs:
	Parsing and typo fixes.
	Fixed game freeze error when using the 'Inspect' action under a slaves' 'Management' tab.
	Fixed incorrect tooltip sizes & formatting for slave jobs.
	Characters who are immobilised in sex scenes can no longer use the 'spread legs' or 'pull hair', 'grab horns', etc. actions.
	Fixed incorrect quick sex description when fucking someone's armpits.
	Minor fixes to dialogue flow in a few places (such as the response tab not resetting to the first one when exiting out of the slave management screen).
	Freedom Certificates no longer disappear when examining them in your inventory.
	Fixed bug where quick loading in the main menu was throwing a background error.
	Fixed issue where some positioning actions were available when they shouldn't have been in 'chair sex' and 'toilet stall' sex positions.
	
---------------------

PATCH NOTES FOR v0.4.9

FriendlyAlienFriend's Artwork (https://twitter.com/thealienfriend):
	Added Oglix (with pregnant variations) and Golix artwork.

Pusspuss's Artwork (https://twitter.com/PusspussARTZ):
	Added Fae & Silvia artwork (with pregnant and multi-boob variations).

Engine/Modding:
	Custom parser targets (i.e. the custom parser ID you assign to an NPC when creating them) are now saved and loaded correctly, meaning that custom NPCs can now be accessed via their custom ID after saving and loading. (More of a bugfix than an addition.)
	Added 'IGNORE_HAIR_RESTRICTION' item tag, for use on clothing which should be able to be equipped into the HAIR slot even if the character has no hair.
	Added 'WEAPON_FIREARM' item tag, which should be given to any weapon that should be regarded as being a firearm. (Weapons with this tag are affected by the new 'Firearms Mastery' perk which Ghost and Hammer have.)
	Added a new 'submitBlocked' element to combat responses, allowing you to disable the option to submit during combat scenes.

Gameplay:
	Added the next section of the main quest, where you get the help from the SWORD Enforcers in Elis. (thanks to DSG for assistance with Enforcer lore)
	At the nightclub, 'The Watering Hole', if you are a demon you can now skip the queue, and if you've sucked Jules's cock, you now can have sex with him in his office.
	Added a new sex toy shop location in Dominion; 'Lovienne's Luxuries'. Sex toys and fetish gear is now sold here instead of by Finch.
	Added new 'doll' race. This race only appears in Lovienne's Luxuries at the moment, and dolls will be available to purchase as a type of slave in the next version.

Clothing/Weapons/Tattoos:
	Added 'cuff choker necklace' (androgynous, neck slot, sold by Nyan).
	Added 'triple cuff choker necklace' (feminine, neck slot, sold by Nyan).
	Added 'balaclava' (androgynous, hair slot (so that it can be equipped with hats, eyewear, and mouth items), sold by Nyan). Muggers will now sometimes spawn wearing a balaclava instead of a bandana.
	Added 'SWORD dagger' (melee, one-handed, 25 base damage with high variance, all damage types, not sold by anyone as it's a special reward).
	Added 'leg warmers' (feminine, calves slot, sold by Nyan).
	Added 'arcane slegehammer' (melee, two-handed, 25 base damage with low variance, all damage types, sold by Vicky).
	Standardised the angle of two-handed melee weapons' icons (battle axe, sledgehamme, and zweihander) to be opposite to that of one-handed weapons.
	Added 'barcode' tattoo.

Other:
	Characters now need to be visibly pregnant (i.e. progressed past the 'risk of pregnancy' stage) in order to lay eggs via ovipositor. (Remember that characters can use mother's milk to progress past this stage if you want to impregnate & lay eggs in the same sex scene.)
	Added the 'Highly illegal' tag to the arcane revolver.
	Friendly occupants now earn experience by working slave jobs (25% chance per hour to earn 5xp).
	NPCs' elementals now show in the 'Characters Present' panel on the right of the screen, even when not active.
	Catherine (the slime queen) now has barbell nipple piercings and a triple cuff choker necklace, as her artwork depicts.
	You can no longer loiter in 'The Crossed Blades' tavern, as doing so could leave you in there during closing hours.
	Added 'light purple' as a skin colour.
	The default fetish preferences for the 'Bimbo' and 'Cross dressing' fetishes has been lowered. (This won't have any effect unless a new 'properties.xml' file is generated, i.e. only on a completely new game start.)
	Changed the masculine/female race names for dobermanns from simply 'dobermann/dobermann' to 'dobermann-boy/dobermann-girl' to make them more consistent with other race names.
	Changed the name postfix of ground floor maps from 'GF' to 'F0', and that of first floor maps from '1F' to 'F1'.
	Added 'flavourless' as a new fluid flavouring.
	Changed default feminine gender names for lacking genitals from 'doll' to 'mannequin'.

Bugs:
	Parsing and typo fixes.
	The awning poles, green cloth, and embroidered sign are now correctly removed from the player's inventory when completing Eisek's stall quest (these items are also removed from your inventory when loading into this version if you've already completed the quest).
	The 'Clean her' option on Nizhoni is now correctly disabled after activating it.
	Fixed issue where the next scene after going downstairs in Elis's town hall would be the scene at the top of the stairs instead of the bottom.
	Fixed some dialogue bugs in Pix's gym where it would describe you as not being a member of the gym when you were and vice versa.
	You will no longer obtain condoms used by NPCs in sex if either the player or the NPC is a spectator of the sex scene and the other one isn't.
	The 'Trickster's Mask' is no longer sold by Nyan (the whole set will be added as a quest reward at a different location in a future version).
	Fixed issue where Nyan was described as saying goodbye to you when you left her store while she wasn't there. 
	In double-penetration sex, penises no longer have their race prefix added to their name to prevent illogical parsing (e.g. 'wolf-cocks' was used for when a wolf and a non-wolf were penetrating).
	The vagina and anus orifices for characters with a cloaca are now correctly treated as being blocked for the purpose of sex action availability when clothing is equipped into them.
	Fixed issue with the 'Apple Pie à la Mode' item sometimes having incorrect colouring.
	The 'Balls focus' sex action now requires the performing character to have a real penis (so this action won't be available for strap-ons anymore).
	Fixed issue where half-demons could load full demon transformation presets but not half-demon ones.
	NPCs which spawn at the bar in 'Lights Out' no longer have their genitals and all other concealed body parts revealed to you right from the start.
	Fixed bug where you could get stuck in Desryth's apartment after rejecting him, then returning to meet him and rejecting him again.
	Fixed bug where if you reloaded a game which was saved during the day, NPCs which had spawned in Elis's alleyway tiles at night would often despawn and disappear.
	Fixed issue in sex actions involving urethral penetration of a penis where a pussy was being incorrectly referenced.
	Condoms now correctly block access to the wearer's penile urethra.
	The quick load feature should now work correctly for characters with a space in their name.
	Fixed bug where if you enchanted an item which had been renamed, the item's name would be reset back to its default name.
	Using the 'Quick sex' sex action now correctly increments your sex stats.
	Fixed bug where Natalya's TF potion wouldn't work if you were a demonic slime.
	Fixed background error being thrown when trying to delete Sterope's sexual partners (which would also leave random NPCs in the stables in the Centaur's Sword tavern - these excess NPCs will be cleaned up upon loading into this version).
	Fixed bug where the 'lime green' colour for clothing would be shown twice in the dye menu, with the second instance not being responsive.
	Fixed bug where you could knock on the door to Minotallys's office and have a conversation with her while she was asleep in her bedroom.
	If you have more 'Quest' rarity items than your inventory tab can normally display, the UI will now display your extra quest items instead of hiding them from you.
	Fixed bug where tooltips for perks weren't working in some character view windows.
	Fixed bug where setting body coverings would not set the correct covering pattern or modifier.

---------------------

PATCH NOTES FOR v0.4.8.9

Engine/Modding:
	The 'imageEquippedName' element in clothing and weapon files now supports parsing, allowing you to change the equipped icon based on who's got it equipped (using 'npc' as the parsing target for the character who's equipping it).

Clothing:
	The 'horseshoes' item is no longer limited to taurs, and is instead only restricted to characters with hoofs.

Other:
	Added an option to completely reset all virginities and virginity loss information in the debug menu (on the second page of the 'stats' tab).
	Added more time options when loitering.

Bugs:
	Fixed bug where you couldn't access your key items page in your inventory.
	Unique items on the floor or in NPCs' inventories are now correctly placed in their unique items tab instead of being mixed in with all other items.
	When clicking on an item in the 'Items Present' section on the right of the UI, the inventory will now open on the correct page for the item that's been clicked on.
	Fixed bug where clicking on the item at the very bottom-right of the inventory grid would change the inventory page to the next one.

---------------------

PATCH NOTES FOR v0.4.8.8

DSG's Eisek Quest:
	Added a new NPC merchant to Elis's Farmer's Market, who also serves to gate early access to the dragon TF behind a quest.
	Added three side quests related to this NPC (with one of these quests being exclusive to silly mode).
	Ralph no longer sells dragonfruit, as this new NPC is now the one who sells it (provided his quest is completed in the best way).
	Added: 5 new clothing items for new NPC outfit; 1 new clothing item for silly mode; 1 new weapon for silly mode; 4 new Items for new NPC to sell; 3 new quests (1 exclusive to silly mode); 4 new quest items (1 exclusive to silly mode).
	Full patch notes and details can be seen in the PR here: https://github.com/Innoxia/liliths-throne-public/pull/1718

Pusspuss's Artwork (https://twitter.com/PusspussARTZ):
	Added artwork for both Wolfgang and Karl.
	Added artwork for Jess, which includes pregnant and multi-boob variations.

Contributors:
	Fixed bug where vaginal, lactation, and virginity fetishes had incorrect sorting (based on left-aligned fetishes being active/giving and right-aligned being passive/receiving) in the fetish menu. (by Maxis010)
	Changed the Body.setFeral() method to not set the body as feral if the subspecies does not have feral attributes or is null. (PR#1771 by SightglassCat)
	Fixed missing background textures in slime and half-demon race icons. (PR#1772 by SightglassCat)
	Added 'winged' to NPC lists and tooltips for winged characters of a race that usually does not have wings. (PR#1724 by Stadler76)
	Made NPCs react more logically to unexpected genitals being revealed in sex scenes, with genital reveals now based on whether the perceived gender of the subject normally has one. (PR#1741 by NoHornyOnMain)
	Enabled tattoo rendering with non-standard colours (e.g. via save editing). (PR#1742 by NoHornyOnMain)
	Fixed issue where setting a character's feral subspecies to null wouldn't display the correct behaviour of reverting their feral status. (by Stadler76)
	Updated the 'LTSuperGuide' which is included in the game's folder. (by C4MG1RL)

Engine/Modding:
	Added 'FITS_MUZZLES_EXCLUSIVE' and 'FITS_BEAKS_EXCLUSIVE' item tags for tagging clothing which can only be equipped on characters with muzzles or beaks.
	Added hook to AbstractItemEffectType values via an 'ITEM_EFFECT_TYPE_' parsing prefix.

Gameplay:
	Added a new character, 'Sterope' to the Enforcer station in Elis, who has some BDSM and feral sex content.

Clothing:
	Added 'Sturdy Steed' clothing set, which provides +5 physique and +25 max health.
	Added: 'Bridle' (androgynous, mouth slot, Sturdy Steed set, only fits muzzles).
	Added: 'Saddle' (androgynous, leg slot, Sturdy Steed set, only fits quadrupedal bodies).
	Added: 'Horseshoes' (androgynous, foot slot, Sturdy Steed set, only fits hoofs, only fits quadrupedal bodies).
	Added: 'Tail bandage' (androgynous, tail slot, Sturdy Steed set).

Combat:
	The two final upgrades to the Vacuum spell no longer strip clothing from unique NPCs. (As stripping clothing from quest-critical NPCs was resulting in issues with their content.)

Sex:
	The 'GenericSexualPartner' NPC class no longer spawns with addictive fluids, so as to prevent issues with their partners getting addicted (which was happening with Jess).
	For size-difference characters, the smaller character can now kiss crotch-boobs in the missionary position, and can now kiss breasts instead of kissing mouth in the mating press position.
	You can now use the 'GENERIC_ORGASM_CREAMPIE' action in masturbation scenes (which is the same action that provides the 'Handjob Climax' orgasm action).
	Added autofellatio and autocunnilingus sex actions, which require the new 'hpermobility' perk to unlock, are limited to non-taurs, and which work in most but not all sex positions.
	Added a small speech variation to the creampie sex action.

Other:
	Both types of wet wipes now additionally clean all equipped clothing.
	You can no longer assign work hours to friendly occupants if they want to sleep during that hour.
	Improved method of calculating sleep hours for slaves and friendly occupants so that they prefer to sleep as close to the mid-point of their natural sleep hours as they can.
	Jess can now be impregnated, and you can pay her (5000 flames) to take a breeder pill before having sex with her. She also no longer has the barren perk nor a hatred of the pregnancy fetish, and also she now refuses to consume items during sex.
	Demons, half-demons, and imps will no longer spawn with demonic horse tails if they're bipedal.
	The 'ladykiller' and 'minx' perks are no longer traits which require equipping to work.
	Added 'hypermobility' perk in the physical perk tree, which unlocks autofellatio and autocunnilingus sex actions.
	Added some dialogue referencing citizens of the Realm travelling over the Endless Sea to new lands (as posters in the nightclub, at the Slavery Administration building, and as a minor piece of dialogue when paying a prostitute's fine to remove them from the game).
	Added Hannah pregnancy reactions to her encounter in 'Lights out'.
	Added a couple of new talk options to Kheiron (one for Fae & Silvia and one for Sterope, both of which require them to have told you when they visit the tavern to be available), and his talk scenes now correctly grey out when they're active.
	Made Fae and Silvia a little taller to better suit their fox-taur form.
	Spotted hyena females no longer spawn in with big clits, and Hannah now has a normal sized clit. (I felt like having every spotted-hyena spawn with a huge clit was too much, but I'm planning on adding a tribe of spotted-hyena-girls with clit-dicks later on.)

Bugs:
	Typo and parsing fixes.
	Fixed game-breaking bug where if you were unable to equip a sex toy which was in your partner's inventory during sex, then clicking on that sex toy would throw background errors and cause the inventory/game to become unresponsive.
	Compacted the compatible slot names in the tooltips for piercing items, so that it doesn't run over into another line and cause the tooltip to overflow.
	Fixed issue where there'd be no slaves in the stocks nor in any of the shops if you entered Slaver Alley before midnight after starting a new game.
	Fixed issue where the Rental Mommy encounter would throw a background (harmless?) error every time it was triggered.
	Fixed bug where the slaves in the stocks and shops in Slaver Alley would sometimes not be saved correctly.
	Fixed bug where exported transformation presets for Elementals which were not bound to arcane or water would cause the transformation preset menu to break.
	Fixed bug where stopping a sex scene in which you were a spectator (such as spying on Rose and Lilaya in Lilaya's lab) would cause the description for that scene to be displayed the next time you used the 'Quick sex' action.
	Astrapi is now always considered to be feminine, ignoring your 'androgynous bodies' setting (as it fits her content for her to always be treated as a 'she').
	Spell tooltips and predictive text in combat now show their potential damage range instead of a random value from within that range.
	Fixed the Vacuum spell's first upgrade downgrading the health shielding debuff from -10 to -5, and also fixed the second and third upgrade tooltips to show their full effects.
	Fixed bug in Helena's custom slave menu where you could customise a slave to be an angel by swapping back and forth between the spinneret tab.
	Lunette's marauders and raiders in the Foloi Fields now have several of their fetish desires set to 'like' instead of 'love', as the 'love' setting was making it look like they had the associated fetish even though they didn't.
	Characters (including the player) can no longer be milked of their cum or girlcum in a milking room if they're wearing any clothing which prevents them from orgasming.
	Removed ability to fight Jhortrax after besting him in the 'Tameshigiri' scene, due to numerous inconsistencies with the resulting post-combat scenes.
	Fixed background error being thrown when completing an incubation pregnancy of a single egg/offspring.
	Fixed bug where transformation presets didn't take into account whether or not the target or preset were of 'short stature', which inadvertently allowed you to transform demons into imps and vice versa by using transformation presets.
	Fixed bug where the greyed-out 'load' button for incompatible transformation presets would still work if you clicked on it.
	Jess will no longer have random fluid addictions (and all of her fluid addictions will be cleared upon loading into this version).
	Fixed bug where if none of the colours defined for an item of clothing within an outfit file were available for that clothing, the clothing would spawn with broken colourings. (This was mostly affecting jewellery on randomly-spawned NPCs.)
	Fixed some inconsistent availabilities of 'offer/request orifice' actions in the breeding stall & glory hole positions.
	Your demonic offspring will no longer spawn with heavily enchanted weapons which would push them over their enchantment capacity.
	Characters in sex who are in the resisting pace and who are involved in finger-anus or finger-vagina sex actions will no longer be described as stimulating their orgasming partner's prostate.
	Fixed bug where after taking a shower in the gym, the text was only shown after you moved away from the tile.
	Fixed incorrect description for the item 'platinum Bank of Dominion card'.
	Fixed bug where you could masturbate in areas in which masturbation/sex was meant to be blocked (such as in the bank).
	Fixed issue where the one-night-stand characters spawning 'Lights Out' would almost always be virgins.
	Fixed minor UI issue with the inventory, where if you dropped or took all items while not on the first page of that inventory, the rendering would mess up.
	Also fixed a related issue where if you took or dropped the last item in an inventory page, the UI would be left on the empty page instead of moving down to the next one.
	Resetting your race via the debug menu no longer clears virginity loss information.
	Filled in some missing virginity location text.
	Fixed issue where use of NPC's hourlyUpdate() method would not handle flag resets correctly, resulting in rare instances of unexpected gameplay behaviour.
	Fixed bug where changing a character's leg configuration would regrow their hymen.

---------------------

PATCH NOTES FOR v0.4.8.3

Bugs:
	Fixed bug where fetishes were not being detected as being owned.
	
---------------------

PATCH NOTES FOR v0.4.8.2

Contributors:
	Fixed issue where player-summoned elementals were not considered part of the player's team for damage calculations, meaning for harder difficulty settings their damage was scaled the same as that of enemies. (by TractorsAttic)
	Fixed parsing bug in Natalya's meeting scene during Helena's romance quest, and fixed a potential NullPointerException related to accessing character present IDs. (by Cognitive Mist)
	Improved getSubspeciesFromBody() method, which makes loading save files significantly faster, especially for large saves in games with many modded subspecies. (PR#1754 by SightglassCat)
	Added 'light red' and changed 'light pink' to 'pink' for salamander scale colours, added missing equip text for the nursing bra, and fixed some inconsistencies in Natayla's new content. (PR#1757 by MintyChip)
	Added pattern support to both micro bikini clothing items. (PR#1759 by DSG)
	Added two new clothing items; 'fedora' (head slot, androgynous, sold by Nyan); and 'trenchcoat' (over-torso slot, androgynous, sold by Nyan). (PR#1761 by DSG)
	Fixed missing IDs and paths for anonymous-classed NPCs. (PR#1762 by SightglassCat)
	Fixed incorrect references to horns in the antenna.xml race mod example file. (by MintyChip)

Image & Character Imports:
	PLEASE NOTE: All imported images for your player character will no longer work, due to the image folder location being changed.
	Custom images for your player character are now stored in the same manner as custom images for non-unique NPCs, that is, in the 'data/images' folder instead of the 'res/images' folder. This allows you to have unique images for your player character in different save game files.

Clothing:
	The Butler's Jacket no longer obscures the finger slot.
	Updated all of the old formatting for clothing displacement/removal text in clothing files.

Sex:
	Moved foot-to-mouth sex actions from the reverse cowgirl position to the cowgirl position.
	Using an ovipositor to lay eggs in someone no longer requires the ovipositor-equipped character to have a vagina (this should only affect slimes, as they're the only race that can get pregnant without having a vagina).

Other:
	Added text to make it more obvious that a slave is losing 1 affection towards you due to being woken up at the start of interacting with them while they're sleeping.
	Elementals are now able to use the save/load transformation menu correctly.
	When loading a TF preset the dialogue scene now moves back to the 'core' TF dialogue, so as to give an indication that the TF has been applied.
	Made the layout of multi-breast option buttons slightly more logical.
	If you've equipped sealed clothing with the 'servitude' enchantment, Lilaya's 'Sealed problem' action will no longer remove all the seals on your clothing, and will instead only remove the 'servitude' enchantments.
	Compacted the layout of the 'subspecies knowledge' perks when viewing a character's perk tree.
	The 'Dungeon Cell' tiles in Lilaya's basement no longer have an upkeep cost (they used to be 10 flames/day).
	In 'Murk's Milker' bad end, the player's tattoos are now removed at the start of the bad end, so as to avoid unexpected transformations occurring during the bad end content.

Bugs:
	Typo & parsing fixes and minor dialogue alterations.
	Fixed bug where Hannah would not return to the bar after encountering her there for the first time.
	Concealed subspecies bonus text no longer inadvertently reveals their race in the tooltip text.
	If a character has the 'Serpent-tailed' leg configuration, any change to the length of their tail is now correctly restored when saving & loading games.
	Added missing 'MURK_BACK' dialogue node in the pregnancy roulette scenes.
	Removed references to the player impregnating Bunny if it was actually Loppy who ended up impregnating her during a threesome.
	Fixed numerous instances of scripting errors related to the change of the NPC.hourlyUpdate() method to take in an int argument (showing as 'Scripting parsing error: X.hourlyUpdate()' in the error.log file).
	Fixed bug where you could bypass the entry fee for Pix's gym if you talked to her and then simply moved forwards into the gym.
	Saving a transformation preset for an elemental will no longer make the save/load transformation menu inaccessible.
	Lilaya will now correctly transform her genitalia back to having a pussy and no cock after sex.
	Fixed issue in Penelope's 'Posters' dialogue where you'd always tell her that you hadn't visited Pix's gym, even if you had.
	Fixed bug where you could assign jobs to guests which were meant to be limited to slaves (which was done by selecting a job category while managing a slave's job, then managing a guest's job and assigning the still-selected job to them).
	Natalya's sex scene in the park is no longer treated as being a public sex scene (as you're behind the bushes and so out of sight).
	Fixed bug where slaves who had sex while working in the kitchen would generate the 'gardener' sex event description.
	When/If you give Scarlett back to Helena, her tattoos are now removed. (This will retroactively apply when loading into this version.)
	Astrapi's pregnancy reaction scene now correctly plays when encountering her at the Elis depot.
	You can no longer teleport into the Crossed Blades tavern (to prevent the player from entering it outside of opening hours).
	Natalya's post-anal-sex dialogue no longer references rimjobs.
	Fixed bug where if you had a fetish temporarily granted via enchanted clothing, the fetish would be permanently applied to the wearer after saving & then loading the game.
	You can no longer pay to have your 'penis' pierced if you have no penis but are wearing a strapon.
	
---------------------

PATCH NOTES FOR v0.4.8

FriendlyAlienFriend's Artwork (https://twitter.com/thealienfriend):
	Added Fyrsia, Jhortrax, and Hyorlyss artwork.
	Added artwork variations for Vanessa/Ms. Cunningham without her shoes on.

Pusspuss's Artwork (https://twitter.com/PusspussARTZ):
	Added Silence & Shadow artwork, with variations for multi-boobs and pregnancy.

Contributors:
	Added ability to let friendly occupants take on some of the more mundane slave jobs (Maid, Security guard, Librarian, Cook, Lab assistant, Office worker, and Waitress). (PR#1560 by Maxis010)
	Removed the need to add content checks to multiple locations when adding new content controlled fetishes. (PR#1600 by Maxis010)
	Fixed bug during sex scenes where a background error could be thrown if an NPC who was not involved in the sex scene tried to equip clothing. (by AceXP)
	Bugfixes for GuestJobs PR after merge. (PR#1755 by Maxis010)
	Added support for separate naming for aquatic subspecies that aren't mer-tailed. (PR#1489 by Stadler76)
	Fixed description of height in alpha-imp description ignoring imperial/metric setting. (by AceXP)

Engine/Modding:
	Added 'SWIMWEAR' item tag, which is meant to be used on clothing to aid in item generation.
	Added a new 'conditional' attribute to the new 'effect' element in items' status effect definition section, allowing you to limit effects to be applied via conditional statement. (See 'res/items/innoxia/pills/fertility.xml' for a commented example.)
	Added FOOD_POOR, FOOD_QUALITY, DRINK_POOR, and DRINK_QUALITY as item tags to give finer control over how much of a buff food and drink items should give to the consumer.
	Added 'EYE_SHAPE_' parsing command to access EyeShape enum values.

Image & Character Imports:
	PLEASE NOTE: All imported images for characters in your game will no longer work, due to a significant restructuring of the folders involved.
	Images imported for characters in your game are now located in a folder that's named corresponding to the character's unique ID, instead of their name, so you can now have different images for different characters who share the same name.
	Images imported for characters in your game are no longer stored in the 'res/images/characters/generic' folder, and are instead now stored within the 'data/images/game_id' folder. The 'game_id' is unique to each of your ongoing games (and takes the form of a large number). This change means that imported character images are now associated only with the game into which they were imported.
	When exporting a character, any custom artwork which they have will be exported into a folder alongside the exported xml file (in 'data/characters').
	When importing a character into a game (as a slave, a clubber, or a lodger), if there's a folder in the same directory as the imported character's xml file, which shares the same name as the imported character's xml file, then all images within that folder are automatically imported for that character.
	
Gameplay:
	You can now invite friendly occupants living in Lilaya's mansion to the spa.
	Added banks to Dominion and Elis. You can create an account in the Dominion bank, and then use the deposit boxes to store and retrieve items and money, as well as generate interest on money stored there.
	After having sex with Vicky three times, she will try to dominate you, and if you submit then it will unlock more content with her.
	Added a new internal map for Pix's gym, added a few extra scenes for Pix, and added a new character (a spotted hyena-girl boxer named Hannah) to the gym.
	Completing Hannah's boxing training unlocks a new bar map in Nightlife, in which you can have one night stands with randomly generated NPCs.

Other:
	Reformatted how status effects to be applied upon consumption are displayed in item tooltips to reduce clutter.
	Added a 'musk' content toggle in the 'Sex & Fetishes' page in the content options, allowing you to enable/disable musky cum/girlcum effects. (On by default.)
	Musky cum and girlcum will now apply a 'marked by musk' status effect (applies +5 resting lust and -1 lust resistance) to anyone who is covered in it during sex.
	Vicky's shop, 'Arcane Arts', is now open from 9:00-17:00 instead of 06:00-22:00.
	Added a 'Never' option to the multi-boob content setting, which makes all randomly-generated and most unique NPCs have only one pair of breasts.
	Changed the 'martial artist' perk to 'brawler', which now gives +5% unarmed damage and +10% physical damage. The 'martial artist' perk is now a unique perk which can be obtained via completing Hannah's training (in Pix's gym).
	Nizhoni's content now has a couple of extra musk-related descriptions (which are only shown if musk content is turned on), and you now also have the option to cast the 'soothing waters' spell (if you know it) to clean her and temporarily remove her musk for the proceeding sex scenes.
	The game's default start date is now 2019, instead of the year of your system's time (i.e. 2023). This is so that in-game events remain chronologically feasible, for example older Enforcers having been Enforcers at the time of the fifth human rebellion in 1988. The starting year can still be changed to whatever you want during the character creation process.
	Pandas now spawn with vertical pupils.
	Elementals can now take on the form of an octopus.

Items:
	Added 'swimming shorts' (masculine, groin slot, sold by Nyan).
	Changed the quality levels for dragon, amazon, angel, and imp drinks, and for dragon, rat, and pig food.
	Added the 'DRINK' tag to several items which should have had it.
	Added 'arcane wet wipes' as an upgraded version of 'wet wipes', which are able to remove the 'marked by musk' effect.

Sex:
	Added 'Stroke belly' as a 'loving' sex action, requiring the target to be visibly pregnant and for positioning to allow the performer's hands to reach the target's stomach. (As it's a loving action, NPCs will only use this if they're not sadistic and their affection towards the target is over 50.)
	NPCs in glory hole sex no longer have access to deny actions (as it's physically impossible for them to restrain their partners who are on the other side of the stall wall).
	Added a 'Rape-play allowed by default' option in the 'Sex & Fetishes' content options, which allows submissive characters in sex who have the 'unwilling fuck-toy' fetish to engage in rape-play without first being given permission to do so. (Off by default.)
	Added clit-to-nipple and clit-to-crotch-boob-nipple sex actions for characters with clits large enough to act as pseudo penises.

Bugs:
	The chest sarashi has been changed back from 'feminine' to 'androgynous'.
	Fixed issue where all slaves in Slaver Alley's stocks and shops would be reset every time you loaded a game.
	The 'vaginal virginity', 'pregnancy', 'pussy slut', 'impregnation', 'cum stud', 'cock stud', and 'breasts' fetishes are now correctly always given to randomly generated NPCs if your related fetish spawn preference is set to 'always'.
	After getting them as slaves, resetting the perks of the four 'Murk's milkers' should now work correctly. (It will also reset their occupation trait from 'kidnapped' to the slave trait.)
	Freeing slaves while they're working in a milking room now correctly handles their clothing resets before freeing them. (i.e. removing pumps and replacing their clothing)
	You can no longer ask Claire for help with dealing with Vengar after you've already cleared out the Rat Warrens.
	NPCs will no longer equip clothing onto spectators during sex.
	Fixed issue where Jhortrax didn't have his katana equipped.
	Fixed bug at the end of Natalya's filly training where she'd take your neck-equipped clothing and not return it to you when she put on your filly choker.
	Fixed vaginal and anal clit tease actions, which were checking availability of the action based on the incorrect character's clit size.
	Fixed an issue where characters would sometimes fail to load into a game when saving/loading.

----------------------

PATCH NOTES FOR v0.4.7.5

FriendlyAlienFriend's Artwork (https://twitter.com/thealienfriend):
	Added artwork for Vanessa/Ms. Cunningham, including pregnant variations.

Davyn's Artwork (https://twitter.com/davyndraw):
	Added artwork for Kalahari (lion-girl bartender in the nightclub, 'The Watering Hole').
	Added artwork for Kruger (lion-boy nightclub owner in 'The Watering Hole').
	
Contributors:
	Fixed issue where mods which accessed the GameCharacter.getAffectionMap() method could cause an error which led to NPCs disappearing after saving/loading. (by CognitiveMist)
	Fixed issue in Meraxis's blowjob and cunnilingus sex scenes, where the game was checking for incorrect fetishes to determine when to end the sex scenes. (by Maxis010)
	Fixed issue where you couldn't change your hairstyle in your room's 'Hairstyle & Makeup' menu. (by Maxis010)
	Fixed bug where certain black-white colouring combinations wouldn't correctly identify someone as a panda-morph. (by CognitiveMist)
	Fixed bug where the 'New Game' button would sometimes not work, requiring a game restart to get it working again. (PR#1752 by CognitiveMist)
	Fixed issue where characters who were imported into a game would remain related to the player (or other characters by chance) if they were related to them in the save where they were exported. (PR#1743 by Maxis010)
	
Engine/Modding:
	Added 'FertilisationType' enum (game/character/pregnancy/FertilisationType.java) to track fertilisation type of Litters.
	Added 'Nocturnality' enum (game/character/race/Nocturnality.java) for assigning nocturnality values to subspecies. For modded subspecies, you can now define the nocturnality of a subspecies within a 'nocturnality' element. Any subspecies missing this value will default to being biurnal.
	Added 'FOOD' and 'DRINK' item tags which should from now on be applied to any modded food or drink items (with the idea being that any effects gained from food or drink can then be applied from any item tagged as such).
	Added an optional 'statusEffects' element to modded item xml files, allowing you to define status effects to be applied when the item's effects are triggered (for a commented example see 'res/items/innoxia/pills/fertility.xml').
	Added a 'rapePlayBannedAtStart' field to sex managers, allowing you to define whether or not NPCs with the 'unwilling fuck-toy' fetish will start sex in the resisting pace (defaults to true, thereby making it so rape-play NPCs no longer start consensual sex scenes in the resisting pace).
	Added 'game.startGenericSex(character)' method to allow quick testing of a generic sex scene between the player and an NPC.
	Moved all hard-coded chest and nipple clothing out into the res folder.

Gameplay:
	You are now able to impregnate Vanessa/Ms. Cunningham by giving her a 'breeder pill' or 'broodmother pill' during sex.
	You can now gain entry to Zaranix's house during the related main quest by repeatedly knocking on the door.
	Eating or drinking (via items or scenes in which you eat/drink) now confers positive status effects; 'recently eaten' and 'thirst quenched', respectively.
	You can now ask Astrapi about being impregnated once her affection towards you is high enough, after which you will be able to get her pregnant.
	Added an encounter in Dominion's park tiles to enable you to discover Natalya outside of Helena quest. It will trigger between 9:00-15:00, if the weather is not an 'arcane storm' or 'stormy sky', if you have travelled to all the park tiles, and if you have either completed Natalya's romance quest or not started it.
	
Lilaya's house/Slave management:
	You can now pick roses from Lilaya's garden (limited to 1 per day).
	Added two new slave jobs; 'gardener' (4 slaves max., location is central courtyard garden); 'security' (8 slaves max., first security guard will always be posted at the entrance, with the others patrolling the corridors, has 'answer door' and 'entrance priority' job settings).
	Added 'dining room' room upgrade, along with another new slave job, 'waiter'. You can choose to order a meal in the dining room, so long as you have slaves working as a cook and waiter.
	Added 'slave lounge' room upgrade. Your slaves will go here when not sleeping.
	Slaves will now sleep during idle time; the hours in which they sleep will depend on their race's nocturnality, and will be displayed in the job management screen via 'zzZ' next to the idle hour slots in which they'll be sleeping.
	Added a new 'Sleeping' permission category, allowing you to specify whether slaves should sleep at night, during the day, or whenever they want (which will be based on their race's nocturnality).
	Added description of slaves present/not present in their room description.
	Friendly occupants will now sleep at times based on their race's nocturnality.

Items:
	The 'breeder pill' and 'broodmother pill' items now disable the effects of menopause while their effects are active.
	Reduced rarity of subspecies books from legendary to rare, so they will now disappear from tiles like ordinary items.
	The 'ribbon' clothing can now be equipped on a character's penis.
	Added 'micro bikini top' and 'micro bikini bottoms'. Both are feminine and sold by Nyan.

Sex:
	NPCs with the 'unwilling fuck-toy' fetish no longer start sex in the resisting pace by default, and must be first allowed to perform rape-play before they'll switch into it. 
	If not satisfied at the end of sex, NPCs now lose 5 affection towards the person who ended the sex scene, instead of towards all dominant participants.
	Improved description of size difference oral availability that's appended to the end of the 'standing' and 'against wall' sex position intros.

Combat:
	The 'All out strike' move now has a critical requirement of being the only move used, instead of being used 3 times (which was impossible due to AP cost).
	Buffed the 'vulnerable' status effect that's applied via 'Hunting call', 'Talon slash', 'scratch', and 'squirrel scratch' from -2 physical shielding to -10 physical shielding and -5 physique.
	The 'Talon slash' combat move now deals 120% of the attacker's unarmed damage, instead of a flat 20.

Other:
	Clothing and weapons of the same rarity are now sorted in inventories so that they're grouped together.
	Added an 'Always' option to the fetish preferences menu, which makes it so that randomly-generated NPCs will always spawn with that fetish.
	The subspecies pages in the encyclopedia now display the subspecies' nocturnality, whether or not they're aquatic, their default leg configuration, and whether or not they're short-statured.
	Slightly improved dialogue flow after both instances of combat in the slime queen's tower, and made it so the slime encounter rate in Submission's tunnels if 4 times higher than normal if you're at the start of the slime queen quest (to make it easier to progress the quest).
	You no longer need to seduce Wolfgang and Karl in the Bounty hunter lodge if you've previously had sex with them (i.e. during the quest in Kay's textiles).
	Added a new 'clothing femininity' option (in 'Content Options' -> 'Gameplay'), allowing you to set clothing femininity values to off, masculine-only, feminine-only, or on.
	The 'pregnancy' tattoo counter now includes the bearer's ongoing pregnancy (if applicable) in the count of how many times they've been impregnated.
	Added 'pregnancy partners' and 'impregnation partners' tattoo counters, which track how many unique partners have impregnated or been impregnated by the bearer, respectively.
	The shady dealer encounter in the alleyways of Dominion will no longer trigger during an arcane storm.
	If you have the 'object of desire' trait active, then Angel (in Angel's Kiss) will wait until she's satisfied before ending the sex scene, instead of ending it as soon as you were satisfied.
	Characters who have large cum expulsion values now spawn with 'stallion' or 'dragon' condoms, so that their condoms don't break in sex.
	The cultist chapels which appear during October in Dominion's streets will no longer spawn in adjacent tiles.
	Added better indication of whether or not sex with slaves in the bathing scene in the spa will be considered rape.
	Eye clothing which blocks eyes (i.e. the blindfold) now correctly conceals the wearer's eyes. (This will only be noticeable if you encounter an NPC who's already wearing a blindfold, as just like genitals & breasts, once you've seen their eyes then they will remain 'known' even if concealed afterwards.)
	Lunexis now has minimum affection towards the player, Meraxis, Aurokaris, and Ursa.
	Added 'Gangbang' options to sex actions when interacting with a slave so that you can more easily start a sex scene with all slaves who are present.
	Added a shaft in the far west of the Bat Caverns which links them to Dominion.
	
Bugs:
	Parsing, typo, and minor dialogue fixes.
	Prevented friendly occupants in Lilaya's mansion from being able to get the 'Mushroom forager' job (it was intended as a background only for offspring found in the Bat Caverns).
	Fixed issue where Lilaya would reference her growing a cock to get you pregnant even if she impregnated you via the effect of Amazon's Secret.
	Fixed bug where slaves could work in the office or milking room while still being stationed in the slavery administration.
	Fixed issue where friendly NPCs having moved out into an apartment, as well as offspring in the alleyways of Dominion, would be affected by arcane storms even though the scenes are described as being inside their apartment.
	Fixed incorrect dialogue being displayed after sex with Wolfgang and Karl in 'Kay's Textiles' during Nyan's quest.
	Fixed background error being thrown when inserting Kay's buttplug.
	Nyan now correctly only wears her weekend outfit (skater dress with no shoes) after she's decided to take weekends off work (i.e. after progressing through her romance quest).
	Fixed bug where the impregnation counter for tattoos would increment even if the impregnating character failed to get their partner pregnant, then decrement once the pregnancy possibility resulted in no pregnancy.
	Tooltips for ongoing sex status effects no longer cut off half-way through displaying information.
	Using quick sex in Astrapi's handjob & armpit scenes now only uses the related handjob/armpit actions. Also using quick sex in Rose's dungeon scene no longer allows her to use her pussy and lose her virginity.
	Fixed issue where feral characters who were transformed into a slime would bug out and be identified as a human.
	Fixed issue where body randomisation for centaurs was not working for all body parts, and would also increase the randomised character's height twice.
	Fixed issue where dirty talk wasn't parsing correctly for random Dominion demon attackers, Kate, and Lilaya.
	Fixed raccoon-morphs having hyena-morph crotch breasts.
	Fixed issue where the transformation menu's buttons for changing urethra elasticity and plasticity would change throat elasticity and plasticity instead.
	Clothing worn by slaves who go to work at a milking room will no longer sometimes completely disappear.
	Added a missing 'RESIST_TRANSFORMED_NO_RAPE' dialogue node in Submission's slime tunnel encounters.
	Fixed bug in the nightclub where if you were a sub and annoyed and then left your partner, the next partner you found would start off at the same level of annoyance as the one you just left.
	Dominant partners in the nightclub will now leave you if you keep on annoying them.
	The random partners during sex scenes while working as a cow in Evelyx's Dairy will no longer have fetish desires or orientations which result in them disliking sex.
	The headless horseman will no longer regain his virginities between encounters.
	Fixed issue where the replacement and displacement descriptions for the 'lowback bodysuit' clothing item were reversed.
	The visibility of an asshole of an NPC who has a cloaca is now correctly linked to the groin area, instead of the ass.
	Fixed bug where all menu buttons, including loading a saved game, would not work during combat.
	Fixed UI issue where some elements which were meant to be shown as disabled, such as forbidden spells, would not render the disabled overlay.
	Fixed incorrect slave references in the sleeping/waking scenes in your bedroom.
	Fixed issue where slaves would be tagged as having orgasmed 24 hours later than intended while working in the milking room (which led to the 'pent up' status effect not activating at the correct time).
	Fixed bug where the cunnilingus demos (giving and receiving) at the cafes in Slaver's Alley would sometimes have their scenes at the start of sex swapped.
	Corrected the penis & cum related part of the orgasm description for when a futa character performs a 'Thigh squeeze' orgasm due to receiving cunnilingus.
	Fixed issue where removing Kay's chastity cage would always display the scene variation for the minimum time of him having been locked up.
	When an NPC forces a transformation on you after losing combat, they will no longer reference a 'no race-cock'.
	Fixed issue where you were able to move after losing to Meraxis's three demon subordinates in her citadel, which was allowing you to access her treasury room and avoid being thrown out.
	Fixed issue where giving yourself 'demonic-owl' eyes as a slime would change your subspecies from slime to owl-morph, thereby preventing you from accessing the self-transformation menu.
	The gryphon's 'Hunting Call' combat move now correctly applies a +20 buff to physique and arcane as described, instead of +15.
	Fixed bug where if you unsealed and unequipped a sealed item of clothing during sex, after sex the clothing would be cloned, with one clone remaining in your inventory and the other being re-equipped onto you.
	If armpit and/or udder content is disabled in your settings, then in the enchanting menu you will no longer see associated fetish or body part options.
	Fixed issue where selecting some transformative potions (such as the pre-made 'Brax's surprise' potion) while they're located in a world tile (i.e. not in a character's inventory) would result in an error being displayed instead of the potion's information.)
	Fixed issue where feeding a spider-morph a caffeinated food or drink item would always intoxicate the provider of the food/drink (which was usually the player) instead of the targeted spider-morph.
	NPCs should no longer be able to equip clothing onto their partners through other clothing during sex (such as equipping a buttplug on their partner if the partner is wearing trousers).
	The 'Wolf-tease' action in Brax's office now works if you're an arctic wolf-girl.
	Fixed issue during Nyan's first sex scene where she couldn't restart giving you a blowjob if you pulled out during orgasm.
	When having submissive sex with a sissified Vengar, her cage is now correctly removed, and she also now correctly continues to wear a slave collar after being sissified.
	NPC names which begin with a non-alphabetic character no longer have 'a' or 'the' automatically appended to the start of their name.
	Upgrading rooms in the dungeon in Lilaya's mansion now correctly charges you the associated upkeep costs.
	Fixed issue with sex action availability between size difference characters in the 'against wall' position (such as when the shorter character was facing the wall they were able to perform oral on the larger character behind them).
	Fixed issue where the encounters while wearing a filly collar in Dominion street tiles were triggering far too frequently.
	If a clothing item can be equipped during sex, but not in every possible slot, then the inventory will no longer show it as greyed-out.

----------------------

PATCH NOTES FOR v0.4.7

Contributors:
	Added more content for Elizabeth (the guard at Lyssieth's palace), including sex content, which starts by meeting her in one of the rooms within the palace between 20:00-23:00. (by AceXP)
	Fixed issue where you'd be unable to change your ass/facial/pubic/underarm hair values in Kate's shop. (by Maxis010)
	Fixed issue where NPCs' 'fleshSubspecies' variable would unintentionally get set to Subspecies.HUMAN, even if it shouldn't be a human. (by Stadler76)
	Fixed some incorrect daughter/son relationship references. (by Lio)
	Fixed bug where stickers for clothing which fitted into multiple slots would not be initialised correctly. (PR#1733 by CognitiveMist)
	Added Maven profiles to auto detect which OS the build is running on. (PR#1732 by AlacoGit)
	Minor optimisations; Added ability to pay to remove prostitutes in Angel's Kiss; Improved several update methods; Racial tooltips are now hidden for characters who have their race hidden; Advanced race knowledge is now required to see racial status effect attributes. (PR#1731 by Maxis010 and CognitiveMist)
	Added the same SVG zLayer, resizing, and rotation functionality to tattoos which was added to clothing/weapons a while ago - see the 'imageName' attribute in the 'res/mods/innoxia/items/tattoos/heartWomb/heartWomb.xml' file for comments on how to use the new functionality. (PR#1739 by NoHornyOnMain)
	Fixed serpent-tailed coatls being named coatl-lamias. (PR#1725 by Stadler76)
	Added 'feral' to litters when giving birth, viewing pregnancy stats or the offspring map. (PR#1723 by Stadler76)
	Added support for loading character .xml files as modded characters (see 'res/mods/modding.txt' for information on how to use this). Also added a small 'shady trader' encounter to Dominion alleyway tiles which uses this new modding functionality. (PR#1716 by AceXP)

Engine/Modding:
	Moved all 'Over-torso' clothing entries from being hard-coded into the external 'res/clothing/innoxia/torsoOver' folder.
	Fixed the isHourBetween() method not working for time ranges which passed midnight.

Gameplay:
	Astrapi can now be impregnated.

Clothing:
	Skirts now need to be pulled up to access the 'thighs' area.
	Improved method for determining which extra items of clothing need to be removed before an item of clothing can be removed, which should prevent issues where items of clothing were blocking one another's removal.
	Improved tooltip for when unequipping/displacing clothing is disabled, so that it tells you which other item of clothing is responsible for preventing the clothing from being unequipped/displaced.

Sex:
	The 'Automatic stripping' content option no longer causes spectating NPCs to be stripped a the start of sex.
	Characters who are in the 'resisting' pace during sex will now correctly respond to an orgasm denial by using the 'Denied!' action.
	When removing the seal on an item and then taking it off during sex, the auto-equip after the sex scene will now trigger the item's sealed state, thereby re-sealing it back onto the character.
	The 'Customer approaches' sex action in Ralph's oral sex scene will now only trigger once every two turns at maximum.
	NPCs will now only equip chastity devices on their sexual partners if they either like or love the denial fetish.
	The 'Desires' status effect tooltip now always uses standard names for sex areas instead of random ones.
	Character who are on all fours can no longer use finger actions on a character who's fucking them from behind.
	Further restricted the desire of NPCs to equip condoms; they now only equip condoms on self/partners if their impregnation/pregnancy fetish is negative, instead of neutral or negative.

Other:
	Slightly improved colours in clothing/tattoo UI.
	The clothing types (such as sex toys and BDSM gear) which NPCs spawn with are now more randomly selected, which should result in NPCs spawning with a broader range of sex toys.
	Encounters are now only checked for after the game has started (to prevent the need for !game.isStarted() in encounter triggers).
	Added tooltips for colours to the 'Add tattoo' UI.
	NPCs will now only spawn with condoms in their inventory if they have the requirements to equip them during sex (i.e. negative towards cum stud/addict fetishes, or negative towards impregnation/pregnancy fetishes).
	Gave the name of 'peryton' to half-demon deers.
	Added a new 'Offspring Encounters' content option (under the 'Gameplay' options), which allows you to enable/disable randomly encountering your offspring.

Bugs:
	Typo, parsing, and formatting fixes, along with some minor text improvements.
	Fixed bug in the self-transformation UI where the buttons that increase/decrease a character's udder/crotchboob lactation were setting the lactation based on the character's regular breast lactation.
	Fixed issue where if an NPC's 'pet name' was 'Mr./Mrs./Miss X', it would not automatically change based on their femininity.
	Slaves who are only wearing milking equipment will no longer be described as taking off their clothes prior to being inspected.
	The imp guards for each of the three demons in Submission's fortresses no longer spawn with condoms/clothing in their inventories, thereby preventing them from interfering in sex scenes with the demons.
	Fixed issue with salamander cum always being called simply 'salamander' instead of 'salamander-cum'.
	Fixed inconsistency in dialogue when submitting to a demon in the alleyways of Dominion, where it was implied that the demon would be growing a cock even though they didn't do that.
	Fixed issue where if you took someone home from the nightclub and you currently had slaves tending to your bedroom, you could end up having sex with a slave instead of the clubber.
	Fixed issue where some of Ralph's unique sex actions didn't have titles.
	Fixed bug where none of the buttons in your inventory would work during combat.
	Possibly fixed an unpredictable bug where an action that starts combat would very rarely not work and require you to load a saved game to work properly.
	Added missing tooltip for the 'Reset' action in combat.
	Fixed minor issue in the main quest where Lilaya would sometimes not be present in her lab during Lyssieth's visit.
	Fixed bug where Meraxis would sometimes be incorrectly placed in Lyssieth's office when loading a saved game.
	The 'femininity' parsing command will now always apply the correct 'a' or 'an' determiner.
	Fixed bug where dying a weapon that's on the floor while having an identical weapon equipped would throw background errors.
	Fixed issue where at the start of sex in which there are X characters, NPCs' area reveal descriptions would be duplicated X times.
	Fixed issue where the guards at the imp fortresses would always act as though they knew you were a demon even if you were appearing as a different race.
	Fixed bug where self-equipping a condom during sex would give a description as though it was being equipped on your partner.
	The sex actions 'Paizuri/Naizuri into mouth' and 'Thrust into mouth' now correctly check to see if the target's mouth is blocked by clothing when checking for availability.
	Fixed bug in sex where it was possible for NPCs to equip clothing on the player or other NPCs even if the equip slot was involved in an ongoing sex action.
	Fixed issue where enchanting an item of clothing which had name prefix or postfixes (such as '(flowers)' or '(blossom)' for the kimono) would duplicate the enchantment prefix/postfix.
	Fixed issue where otters were having their hair covering set to otter fur instead of hair.
	Demon attackers in the alleyways in Dominion are now correctly spawned with the 'mugger' background.

----------------------

PATCH NOTES FOR v0.4.6.7

FriendlyAlienFriend's Artwork (https://twitter.com/thealienfriend):
	Added artwork for Astrapi, including pregnant and crotch-boob variations. (Crotch boobs will be shown if your 'Crotch-boob & Udder Content' content setting is turned on.)
	Added artwork for Vronti.

Contributors:
	Fixed a significant amount of typos and grammatical errors. (PR#1701 by Lis)
	Significant rework and refactor of Controller classes, improved UI handling, and added a 4th +/- button to the fluid storage and regeneration transformation menus. (PR#1713 by Maxis010)
	Fixed issue where subspecies changes for dragons, coatls, and gryphons didn't account for taur/lamia leg configurations when assigning minimum wing size. (by MintyChip)
	Added 'banana' as a new fluid flavouring. (PR#1696 by DSG)
	Added mythical 'salamander' race, with two subspecies; 'flame salamanders' and 'frost salamanders'. (PR#1707 by MintyChip)
	Added 'panda' as a subspecies to the 'bear' race. (PR#1697 by DSG)
	Balanced the flame value calculations for enchanted items, clothing and weapons. (PR#1695 by Maxis010)
	Improved error reporting for parser state errors and improved the parser so that it skips svg files within the parsed input. (PR#1690 by CognitiveMist)
	Added a specific flag to indicate the player's lilin heritage rather than just checking if they are a demon. (PR#1688 by MintyChip)
	Added fetish selection options to sexual experience menu during the prologue's character creation process. (PR#1687 by MintyChip)
	Added Java vendor and basic OS information to error.log to help improve troubleshooting. (by CognitiveMist)
	Fixed grammatical issues in the alligator-morph's racial descriptions. (PR#1685 by Maymay)
	Fixed a cause of the issue where NPCs self-equipping condoms would react as though someone else had equipped the condom. (by Maxis010)
	Fixed bug where a character with an aquatic-tailed lower body would have their leg and feet equipment incorrectly blocked and unblocked, due to the wrong status effects being checked. (by Stadler)
	Added 'latex leggings' (feminine, leg slot, sold by Finch, latex lover set). (by Sage)
	Fixed issue with some buttons in Kate's cosmetics dialogues being unresponsive. (by Maxis010)
	Made LT runnable directly on the most recent Java LTS (17) and created an automatic build and release pipeline to reduce workload using Maven. Also fixed several opaque elements which were supposed to be transparent. (PR#1684 by Tazze)
	Added the ability to choose either the feminine or masculine Enforcer's uniform when progressing past Brax's stage of the main quest. (PR#1721 by Nonny5Mouse)
	Enabled setting furry level for salamander spawns. (PR#1730 by Stadler)
	Replaced an instance of a deprecated newInstance() method. (by AceXP)

Gameplay:
	Added bad ends to losing combat against the harpy matriarchs in the Harpy Nests.

Sex:
	Characters with a spinneret can now only apply webbing to themselves or their sexual partners if they have the related permission to manage their own/others clothing.
	NPCs will now only equip condoms to themselves or their partners if they dislike the associated 'cum stud' or 'cum addict' fetishes. Previous behaviour was to equip if they disliked or were neutral to the fetishes, so this should reduce the amount of NPCs wanting to equip condoms. 
	NPCs will now only equip BDSM or latex gear onto their partners if they like or love the 'bondage applier' fetish.
	If Meraxis doesn't have a fetish that's associated with her post-duel sex scenes, she will now end sex after she's orgasmed once, instead of when the player has orgasmed once, thereby always giving you the opportunity to influence her fetishes when she orgasms.

Other:
	The 'Crotch-boobs & Udders' body setting now only applies to randomly-generated NPCs at the moment of their creation (as was stated in the option's tooltip), allowing all characters to gain crotch-boobs/udders via TF no matter the setting.
	Added a new 'Crotch-boob & Udder Content' setting in the 'Sex & Fetishes' content options to enable/disable udder-related sex actions and udder transformations to be inflicted upon the player. (Enabled by default.)
	Darkened inventory slot icons in the tattoo view panel to differentiate it from normal inventory view.
	Added finer control over sex experience count in character creation and custom slave ordering screens, added anilingus experience, and made it so anal sex experiences are hidden if anal content is disabled.

Bugs:
	Parsing fixes.
	Fixed several rendering issue with the buyback menu.
	Fixed issue where the women's watch in character creation had random primary and secondary colours.
	Fixed bug where penile virginity losses would be reset at the end of character creation.
	World and place names in the UI are now correctly parsed.
	Fixed issue in the 'owned by random NPC' content, where when the NPC took you to get tattooed, the tattoo in the 'lower abdomen' slot would work fine, but the one in the 'lower back' slot would never be given.
	Fixed bug in the post-fight scenes when encountering centauresses in Themiscyra, where sometimes Aurokaris would be identified by the game as being one of the two centauress attackers.
	Fixed issue where unequipping clothing when multiple layers were covering the clothing to be unequipped would sometimes not work correctly. (This is likely still slightly bugged, but I will properly fix it for the update.)
	Fixed issue where imported characters would sometimes fail to load in correctly.
	Fixed causes of the issue where Dominion-alley-demons, cultists, Kate, and Ralph would react to self-equipping condoms as though someone else had equipped the condom.
	The special 'beer barrel' and 'Hazmat Rat Vending Machine' clothing items will no longer potentially be equipped to randomly spawned NPCs, or show up as random loot in alleyway tiles.
	Fixed issue where Rose's sex preferences would ignore your anal content setting in the sex scene after being discovered by her in Lilaya's room.
	Fixed bug where molesting a slave who has the 'unwilling fuck-toy' or 'submissive' fetishes would cause an affection loss, despite the description saying otherwise.

----------------------

PATCH NOTES FOR v0.4.6.3

Contributors:
	Fixed issue where combat would sometimes become unresponsive when your companion (most likely your fire elemental) was under the effect of 'Aura Burn'. This also addressed an issue where combat status effects were being added to all NPCs upon game load and not cleared until after that NPC had been in combat. (by CognitiveMist and Maxis010)
	Fixed bug in the slavery UI where the Affection & Obedience gain/loss would randomly change to unrelated amounts on unrelated jobs when interacting with any buttons. (by Maxis010)
	Added regular arms and back wings to the raptor race. (PR#1712 by DSG)
	Typo fixes. (PR#1711 by DuskitGalager)
	Set the leopard, snow-leopard, and tiger subspecies icons to use the corresponding icons. (PR#1708 by MintyChip)
	Improved default critical hit tooltips and logic, as the default 'crit on third use' effect was a bit ambiguous and unpredictable. (PR#1706 by CognitiveMist)

Engine/Modding:
	Moved hard-coded tattoo types out into the res folder (located at 'res/tattoos/innoxia').
	Added ability to set default colours for tattoo mods (see 'res/mods/innoxia/items/tattoos/heartWomb/hear_womb.xml' for a commented example).
	Added 'PENIS' and 'VAGINA' to ClothingAccess values, allowing you to define clothing as requiring access to the wearer's penis or vagina in order to be equipped (as the existing 'GROIN' value was not specific enough for these slots). If VAGINA or PENIS are defined as a 'bodyPart' in 'blockedBodyParts', these new values will automatically be added, so refactoring of clothing files should not be required.
	Made several optimisations to save game formatting, which should result in quicker load times and smaller save files. (Testing a gigantic save file reduced size by 20% and slightly reduced loading time.)
	Mod folders are now listed at the top of the error.log file (to assist in troubleshooting bug reports).

Gameplay:
	Added vending machines to the entrance tiles in Submission, and added a vending machine discount card as an additional reward to completing the slime queen side quest (this is added to your inventory if you've already completed it when loading into this version).

Clothing/Items:
	All BDSM and latex clothing now has the 'ENABLE_SEX_EQUIP' tag.
	The tooltip for filled condoms now lists how much cum is in the condom, whose cum it is (so long as the cum provider has not been removed from the game), and what flavour/modifiers the cum has.

Sex:
	NPCs will now use condoms in their inventory by equipping them on their partner's penis. (They will not use condoms if they like the associated cum fetish, like getting pregnant, or lack permission to manage clothing.)
	NPCs will now be able to equip any clothing that's tagged as 'ENABLE_SEX_EQUIP' onto their partners during sex. This requires the NPC to be the dom, their partner to be a sub, and the clothing to not interfere with their sex preferences (i.e. NPCs will not equip chastity cages on their partner if they want to use their partner's cock). BDSM and latex clothing will only be equipped by NPCs who have a positive desire towards the 'bondage applier' fetish.
	NPCs who don't have a positive desire towards receiving anal will no longer generate 'receiving anal' sex preferences, and NPCs who have a negative desire towards giving anal will likewise no longer generate 'giving anal' sex preferences.

Other:
	Added tattoos to the debug's item view menu (as the final option, after piercings).
	Applied transformations, clothing, and tattoo changes to all characters involved in Lunexis's bad ends to reflect what's happened to them in the dialogue.
	Non-unique, non-slave NPCs will now generate condoms in their inventory (when time passes into a new day) if they have a penis or vagina, are neutral towards or dislike associated cum fetish, are neutral towards or dislike impregnating/getting pregnant, and are are neutral towards or dislike the giving or receiving penis fetishes.
	The 'Multi breasts' setting now only affects the number of breast rows a character is given at the time of their creation, allowing characters to gain more breast rows via transformations regardless of what this preference is set to.
	Having a 'massive' lip size no longer causes a character to have a lisp (only the 'gigantic' and 'absurdly colossal' sizes apply a lisp now).
	When using a potion to transform the type of an NPC's penis, vagina, ass, breast, or crotch-boob, the NPC's affected area will be set as being known to you.
	Training at Pix's gym no longer rewards you with potentially infinite physical perk points, and instead via training with Pix (unlocked after paying to become a gym member) you can earn a one-off unique perk.
	
Bugs:
	Typo, parsing, and formatting fixes.
	Fixed bug where even after 'tipping' enough to extend the opening hours for The Creamy Bakery to 07:00-17:00, it would still only let you enter between 09:00-15:00.
	Fixed issue where newly imported characters at the nightclub could sometimes be marked as having already been encountered that day.
	Fixed bug which was causing all of the slavery 'pill' permissions to do nothing.
	Fixed issue where slaves would not properly end their jobs if the player was present in their tile either during the hour of their job ending or the hour prior to that. (This is what was causing milking pumps to sometimes remain on slaves after they'd left the milking room.)
	Slightly improved tattoo tooltip height.
	Fixed rendering issue where the 'ears' slot for tattoos would display as being blocked if the character had no hair.
	Fixed bug where slaves in the shops in Slaver Alley would always be generated with a gender based on user preferences, instead of using a gender that's applicable to their shop.
	The 'style.random' parsing argument now correctly trims whitespace.
	Fixed issue where most groin clothing (i.e. underwear) would not prevent clothing from being equipped into/onto the wearer's vagina or penis (e.g. underwear would not block the equipping or removal of condoms, dildos, etc.).
	Using the 'Quick sex' action now correctly handles condom effects from both partners upon orgasm, instead of only handling it if the sex type involved a penis.
	The latex bodysuit and latex corset now require access to a character's wait in order to be equipped.
	The 'Freedom Certification' item now correctly displays it as being consumed on use.
	Fixed harmless(?) background error sometimes being thrown when setting a slave free.
	After a slave has been removed from the game (such as when using the 'Freedom Certification'), the occupancy ledger should now correctly display events which involved that deleted slave without throwing background errors.
	Fixed bug where filled webbing condoms would forget all attributes associated with their cum storage after performing a save and reload.
	Fixed issue where using the quick-load hotkey would result in the game performing a quick-load twice, thereby doubling the time it took to load your saved game.
	Significantly improved the time it takes to use the 'arcane offspring map', which should be noticeable in games where the player has hundreds (or even thousands) of offspring.
	Fixed bug where NPCs in the harpy nests were not being affected by the effects of arcane storms, with the tooltip saying that they were too far away from it to suffer the storm's full effects.
	Fixed bug in Lyssieth's demon TF sex scene, where if you had a penis and no vagina in the final 'sixty-nine' position, Lyssieth would not fully finish your demon TF at the end of sex, leaving you as a half-demon. (If you have experienced this bug in a previous version, you can use the debug menu's 'Race resets' options to turn yourself into a greater demon to fix it. Type 'buggy' at any point to open the debug menu.)
	Fixed issue where if you were immobilised in sex (e.g. from being cocooned), and your partner offered you an item (such as a pill), there would be no actions to choose from, effectively soft-locking the game.
	Fixed issue in some sex scenes where if the player's orgasms were being denied, then the sex scene would never end (e.g. sex scenes in slaver alley's cafes).
	Fixed issue where the yellow highlighting which indicates that you have perk points to spend would not be removed if you opened and closed the perk menu via clicking on your name in the top-left of the UI rather than through the phone menu.
	Fixed bug where loading a game which was saved in a version prior to v0.3.7.8 would cause a background error to be thrown when attempting to open inventories.
	Fixed background parsing errors sometimes being thrown when loading a saved game (related to insufficient checks in the Vagina.setLabiaSize() method).
	Transforming a character into a taur will no longer pass the 'short stature' cutoff, meaning that imps cannot transform into demons and vice-versa when transforming leg configurations.
	
----------------------

PATCH NOTES FOR v0.4.6

Contributors:
	Several typo and grammatical fixes. (by AceXP)
	Fixed issue where demon x human half-demon offspring would incorrectly be generated as imps instead of human half-demons. (by Maxis010)
	Fixed bug where keybind hints with pound or euro keys would not render correctly. (by Cognitive Mist)
	Fixed some parsing issues in the body overview page. (by CognitiveMist)
	Fixed bug where slaves with a newly-assigned job would not leave Slaver Alley immediately, and a UI bug where slaves' affection would not immediately account for changes in overworked status effects. (by Maxis010)
	Milking bug fix where if you didn't auto-sell the fluids, the milking room added the value to your slave profits and then you could the sell the fluids for a 2nd payout. (by Maxis010 - This bug was fixed in the last release but not mentioned in patch notes.) 
	Fixed bug where random encounters could only ever trigger on the first tile travelled through when using the 'walk' fast travel options. (by Maxis010 and Lis)

Engine/Modding:
	Added support for modded subspecies to define a pool of names for random characters of the associated subspecies to use. (See 'res/mods/innoxia/race/hyena/names.xml' for a commented example.)
	Made a very tiny optimisation so that combat status effects are not checked during the update loop if the game is not in combat.
	Added more 'SubspeciesSpawnRarity' values, allowing for a little finer control over how often modded subspecies spawn. (I also renamed the existing values, but the old names are all compatible with the new system, so no refactoring is necessary.)
	Added a new 'unique' attribute to the 'availabilityRequirements' element in tattoo mod files, allowing you to define tattoos as being unique (thereby preventing them from being given to randomly-spawned NPCs).
	If debug mode is on, you can now see the contents of the 'Empty' map region in the phone's map pages.
	Added an 'elementalsAreAllies' attribute to combat responses in modded dialogue nodes, allowing you to set whether or not the player's elemental joins in on a fight.

Gameplay:
	Added ability to import characters as either dominant or submissive partners in Dominion's nightclub, 'The Watering Hole'.
	Added a small amount of content to the cafes in Slaver Alley to make them a little more interesting.
	Added the final bad end content for Lunexis in the Amazons' camp.

Combat:
	The 'Horn headbutt' and 'Antler headbutt' combat moves now critically strike if the attacker is at least 50% taller than the target, and have had their 'dazed' status effect application reduced from 3 to 2 turns.
	The 'Tail swipe' combat move now critically strikes when the attacker's tail has a girth of at least 'thick', and has had its 'dazed' status effect application reduced from 3 to 2 turns.
	All combat moves derived from body parts (such as 'tail swipe', 'horn headbutt', 'savage attack', etc.) now apply critical damage in the same way that normal attacks do when critically hitting their target.

Sex:
	The ovipositor ability for appropriately-transformed penises and clits is no longer tied to an orgasm action, and instead a 'Lay eggs' action is now always available whenever the conditions for laying eggs in an orifice are met.
	Added support for tails to act as ovipositors, and added a 'demonic ovipositor' tail type which can use this new functionality. (Tail ovipositors additionally now enable you to lay eggs in yourself.)
	You no longer need an egg-laying vagina type to lay eggs via an ovipositor in sex. (While you do still need to be pregnant to use this ability for now, I am planning on adding functionality for laying unfertilised eggs in a future update.)
	Characters now prioritise unequipping their clothing into their inventory instead of onto the floor, which should help to prevent the issue of clothing being lost into the void when unequipped onto the floor of a cell that already had a full inventory.

Other:
	Enabled the use of the 'Stop watching' action in the 'Spy on them' Lilaya x Rose voyeurism scene.
	Randomly-generated NPCs now have a chance to spawn with tattoos.
	Improved the visibility of the player icon on the minimap by giving it a slightly darker border.
	The 'Controlled Aggression' perk (from choosing the soldier background) now applies a 1-turn status effect at the start of combat to make it more obvious that the double damage effect is only lasting for the first turn of combat.
	Improved the way that bimbo talk is applied to characters' dialogue; repeat phrases are no longer generated (such as 'like, like'), sentences ending in '?!' are handled correctly, and odd word replacement at comma locations has been fixed.
	You can now teleport out of the Amazons' camp, but still cannot teleport into it.
	Slightly reduced the min/max diameter comfort range of orifice capacities so as to better align them with the recent reductions to penetration girth values.
	Renamed the 'drill hair' style to 'ojou ringlets'.
	The player's elemental is no longer involved in the 'Meraxis duel' and 'Aurokaris sparring' fights.
	Added 'broodmother pill' as a new slave permission setting, and renamed the pills category from 'pregnancy' to 'pills'.
	Added a new 'pregnancy' slave permission category, which has settings for allowing birth, allowing egg laying, and consuming mother's milk (to speed up pregnancy).

Bugs:
	Typo & grammatical fixes.
	Ursa no longer hates the 'penis receiving' fetish, to fix issues where she'd react with disgust towards the player during sex even though she initiated sex with you.
	Fixed issue where you could change positions in Ursa's sex scene.
	Fixed 'honey bread', 'popcorn', and 'berry soda' items not restoring the correct amount of health/mana that was stated in their descriptions.
	When starting a new game with an imported character who already has a weapon equipped, the demonstone that you gain at the start is now added to your inventory instead of being equipped.
	The 'Clit attention' sex action can now correctly be used while receiving cunnilingus.
	Fixed issue where permanent combat status effects would get a negative turn count at the bottom of their tooltip.
	Fixed background error sometimes being thrown when no encounter could be found for a tile.
	Fixed issue where skin colour preferences would not be applied to some randomly-generated characters, such as those spawned via the debug menu's 'spawn attacker' action.
	Fixed bug in sex scenes where NPCs who hate the masturbating fetish would get stuck at 100 arousal and never orgasm if they were in a spectator slot.
	After characters have had their clothing placed in the 'holding inventory' and then restored (such as after bathing in the spa), the 'holdingClothing' element in their save files will now be cleared.
	Using the debug menu to obtain a slaver license now correctly completes all stages of the associated side quest, granting you the slaver license item in the process.
	Using the debug menu to skip Dominion quests now correctly also completes the slaver license side quest (the completion of which is required to be able to obtain Scarlett from Helena).
	Characters on all fours in the 'all fours' sex position can no longer use 'hand to upper-torso' interaction with characters kneeling behind them, and also can no longer cum onto the groin of the person behind them.
	Fixed bug where if a character had a fetish via wearing enchanted clothing, they'd be permanently granted that fetish if they gained a fetish experience level while wearing the clothing.
	Removed incorrect reference to Brax having bleach-blonde hair during his Brandi transformation scene.
	In the stats screen, the 'Physical shielding' stat now correctly takes into account how much physical shielding has been gained via clothing and weapons.
	In sex scenes, immobilised characters who have their orgasms denied now correctly have access to the 'Denied!' action, allowing them to be repeatedly denied without having to release and then re-immobilise them.
	Fixed incorrect health restoration values for Raptor energy bar, Vodka, Two-Tone Slushie, Fish and Chips, and Ink Vodka.
	The 'Power of Suggestion' upgrade to the 'Telepathic Communication' spell now correctly lists the affected combat move as 'Tease', and also correctly applies the negative status effect for 2 turns on the target as stated, instead of 3.
	Fixed bug where after having sex with Oglix, you could teleport into her room and as such explore the VIP area.
	Fixed issue where the option to decline sex with Oglix after flirting with her was not being displayed, effectively forcing you to always have sex with her after flirting.
	Fixed bug where if you'd completed the 'Angry Harpies' quest (to pacify the harpy nests), harpies would no longer attack you in the nests during a storm.
	Fixed issue where threesome sex after beating Enforcer patrols would put one of the Enforcers in a spectator slot instead of an active sex slot.
	Fixed issue where Lunexis and Aurokaris would remain in Minotallys' office after the Themiscyra quest was completed (if Aurokaris and Lunexis are stuck in the town hall in your save, it will be fixed when loading into this version).
	Corrected numerous instances of sex scenes wich start with you choosing to 'Submit' being tagged as being non-consensual.
	Fixed several instances of measurement descriptions not taking into account your imperial/metric preferences.
	Fixed issue where critically-hitting combat moves would not apply their status effects.
	Fixed the description at the start of slave sex where slaves were described as being forced to crawl everywhere when they didn't have that permission set and vice-versa.
	Fixed bug where if you tried to move a slave to a new room before an hour had passed since loading your game, the slave wouldn't be moved to the room.
	Attribute values are no longer rounded up for display in the UI, which should fix some incorrect readings, such as when in sex arousal could display as 100 even if the character was not yet ready for orgasm.
	The racial book for the deer race is now called 'Harts and Hinds' instead of sharing 'Bleating Headbutters' with the goat race.
	The offspring map can now only be used in empty tiles, thereby preventing you from spaning an offspring on a tile that's aleady taken by a randomly-generated NPC.
	The offspring map now works during daytime in Elis's alleyways.
	Aurokaris's 'breasts' and 'ass' ambrosia tasting scenes now use the correct sex positions.
	Dog-morphs will no longer spawn with 'fluffy' fur (although they can still transform their fur to be 'fluffy' afterwards) to prevent them from accidentally spawning as samoyed-morphs.
	Fixed bug where arcane storm effects would not be applied correctly, resulting in NPCs from Elis never being vulnerable to arcane storms, even if they were brought over to Dominion.
	Fixed issue where you could still choose to be vaginally trained as a cock-sleeve in Lunexis's bad end if you didn't have a vagina.
	
----------------------

PATCH NOTES FOR v0.4.5.5

Artwork:
	Added new artwork for Nyan, by Davyn. (Davyn's twitter: https://twitter.com/davyndraw)

Contributors:
	Fixed bug where the game would freeze and break when having sex with a slave in a milking room while all of your milking rooms were full. (by Maxis010)
	Fixed two related bugs where items (such as enchanted elixirs) would not stack correctly after saving/reloading, and where one or more of these separate stacks would disappear upon another save and reload. (by Maxis010)
	Fixed bug where the 'In Control' perk (from the 'teacher' background) would triple negative obedience changes instead of just the positive changes as the job describes, and also fixed issue where changes would be tripled twice. (by Maxis010)
	Fixed issue where you could encounter a softlock when accessing your phone or options menus while in the 'Set alarm' dialogue. (by Cognitive Mist)
	Tracked down numerous elusive bugs. (by Maymay)
	Fixed an issue where if you saved an elemental transformation preset then the TF preset menu would crash with a null pointer. (by Maxis010)
	Fixed issue where the game could potentially get stuck in a loop when exiting the Unit Preferences menu. (by Maxis010)
	Fixed bug where removing an NPC who had summoned their elemental would cause games that are saved after that to crash upon being loaded. (by Cognitive Mist)
	Fixed issue with incorrectly defined dialogue IDs in Lunexis's bad end scenes. (by AceXP)

Maxis010's 'Milk Tax' Contribution (PR#1626):
	Affection gains for overworked slaves have been reduced.
	Base value of milk, cum, and girlcum are no longer affected by fluid modifiers or flavours, resulting in a potentialyl significant decrease in the amount of money that can be earned from milking slaves.
	Affection gains via fetishes from being milked now correctly account for whether it's milk or cum that's being milked.
	Fixed issue where milk slaves' clothing could potentially be duplicated.
	Increased upkeep costs for all milk room upgrades.

Engine/Modding:
	Added new item tag, 'ELIS_ALLEYWAY_SPAWN' and 'ALL_AREAS_SPAWN', which mark items/weapons/clothing as being able to randomly spawn in encounters in the Foloi Fields and in every area of the game, respectively.

Gameplay:
	Added content for the Amazons' camp in Elis (which appears after completing the Themiscyra section of the main quest).
	Added 'deer' as a race, with associated drink, 'Glade Springs', and food, 'Tree Shoots Salad'.

Items:
	In random encounters, racial items for badgers, goats, and sheep will now only spawn in Elis, while racial items for cows, mice, pigs, rabbits, raptors, and wolves will now additionally spawn in Elis.

Body:
	Added diameter value to the 'Penis Length', 'Clitoris Length', and 'Tail Length' elements in the transformation menu.
	Added value of expelled cum to the 'Cum Expulsion' element in the transformation menu.
	Cum expulsion values which correspond to 'large', 'huge', 'extreme', and 'monstrous' cum storage values now dirty 1, 2, 4, and 8 additional inventory slots of targeted characters during orgasms.
	When transforming a character's leg configuration into 'quadrupedal', 'arachnid', or 'avian' from any of the other configurations, that character will gain 33% extra height (the 33% increase is reverted when transforming the other way).

Combat:
	Added 'cycle target' and 'clear target' actions to the 'Commands' tab in combat, giving you control over who your allies are targeting.

Sex:
	Any body areas or clothing which are dirtied by cum upon a targeted orgasm are now appended to the orgasm description.
	Any body areas or clothing which are dirtied by squirting when the orgasming character's vagina is concealed, or when a parter is performing cunnilingus on them, are now appended to the orgasm description.
	Added a minor variation to orgasm descriptions for when a squirting character is being penetrated.
	Using the 'Unequip all' action in sex will no longer unequip condoms.
	The 'object of desire' perk's effect to make participants in sex need an extra orgasm before being satisfied no longer stacks when multiple participants have this perk, and the effect is no longer applied from spectators.

Other:
	Added the option to take either the dominant or submissive role in the sex scene in the museum during the prologue.
	Added an extra pre-fight option for the Lunexis encounter in Themiscyra, which allows you to skip the fight and avoid the negative affection hit with Ursa, Aurokairs, and Meraxis if you have the 'sacrificial shielding' perk equipped.
	Improved wording in the description of the 'controlled aggression' perk to make it clear that your damage is doubled only during the first turn of combat.
	If you have quicksaved at least once, the quickload feature will now load the last quicksave you made, instead of the quicksave which matches your character's current name.
	
Bugs:
	Typo and parsing fixes.
	The information icons in the fetish preference options page now correctly display tooltips when moused over.
	Reducing cum storage via the TF menu now correctly reduces the character's currently stored cum value to the new maximum.
	When being transformed into a demon, all relevant 'Elder lilin's power' perks will now be upgraded into their demonic versions, not just Lyssieth's.
	Fixed bug in the 'defeated by raiders' scene in Thymescria, where the raiders would fuck you and Aurokaris without first growing cocks before the scene started.
	Aurokaris now correctly starts sex scenes with raiders in the 'resisting' pace (unless non-con is turned off).
	The raiders in Themiscyra will now correctly end the sex scene as soon as they're satisfied, instead of waiting to satisfy you and Aurokaris before ending it.
	Fixed issue in combat where NPCs would sometimes target combatants who had already been defeated.
	Fixed bug where orgasming in Lilaya's sex scene while wearing a condom would result in your orgasm actions being unresponsive.
	Fixed bug where fetish combat moves would be unequipped during sex scenes if any sex action related to the fetish was performed.
	Tattoos with a 'none' icon type will no longer incorrectly state that they're 'primarily coloured grey' in the selfie/character page description.
	Fixed issue where offspring would be born with randomly-coloured eyes, hair, and other coverings, instead of having thse colours inherited from their parents.
	Removed the ability to fly in the demon fortresses in Submission to prevent an issue where you could fly past Meraxis and take her gear before encountering her.
	In the custom slave ordering screen (from Helena after completing her quest), parts of the slave's body are no longer concealed during the final character overview.
	Fixed bug where milk slaves would not identify a milking room as being free if you were standing in it and there were already 7 other characters present.
	Fixed bug where slaves would move between milking rooms during their job hours, instead of remaining in the same room for the duration of their work.
	Fixed issue where racial items were not being marked as being available to be found in 'item found' encounters.

----------------------

PATCH NOTES FOR v0.4.5

Contributors:
	Fixed issue where Amazonian Ambrosia wouldn't be given to the player upon searching the district in Themiscyra. (by AceXP)
	Fixed bug in the 'Lilaya's panties' content, where in the threesome section of the sex scene, selecting the 'Lilaya's pussy' or 'Lilaya's cock' actions would not work. (by AceXP)
	Parsing fix in the tooltip for the 'Moo mode' action in the debug menu. (by AceXP)
	Typo fixes. (PR#1680 by Thernn)
	Removed a duplicate line. (PR#1683 by IjyiH)
	
Gameplay:
	Filled in final placeholders in the new Themiscyra main quest content and fixed a couple of minor parsing issues in it.
	
Sex:
	Characters who are taurs can now use the 'sitting in lap' slot in the 'sitting' sex position (described as them turning around and lowering their rear half down into the sitting character's lap).
	Added a minor description variation for vaginal orgasms that are triggered while engaged in tribbing.

Other:
	Appended a numerical value to affection descriptions in the character view screen, so that it's easier to track exactly what affection values an NPC has towards you and other NPCs.
	A character's testicles' covering type is now determined by the testicle type's defined covering, instead of using the character's torso covering type.
	Added variations to the scenes relating to Lilaya's negative reaction to being impregnated for if the player has impregnated her via use of Amazon's Secret.
	Added tooltip to the 'load' buttons in the preset transformation save/load screen, to let you know exactly why a preset transformation is unavailable.
	Dominant contacts at 'The Watering Hole' no longer have their affection reset to 5 when encountering them another night.
	The five stages of the 'intoxicated' status effect now apply an increasing boost to corruption at each level.
	Added horn length to the 'Head & Throat' stats in the phone's body stats screen.
	Reduced the diameter of penises & clits, with reductions being minor for more normal penis lengths, and more significant for longer lengths. (Diameter can still be increased to absurd levels by increasing girth via transformations.)
	Added pregnancy reactions to the harpy matriarch dialogues, and allowed their companions to be impregnated.
	
Bugs:
	Typo fixes.
	The NPC who you encounter during the event while wearing a rental mommy/daddy t-shirt will no longer be gynephilic or androphilic if the player character is masculine or feminine, respectively.
	Fixed issue with missing dialogue for a cunnilingus scene during the 'random NPC's bitch' content.
	Added a catch to avoid a background error being thrown for if a condom has somehow had its cum variable reset to null.
	Fixed several instances, mostly in the titles of dialogue scenes while interacting with slaves, where an incorrect name for the NPC being interacted with was being displayed.
	The Amazon's Secret item will now correctly apply the 'feminine fertility' status effect to the consuming character.
	Fixed some formatting issues with tattoo descriptions at the bottom of the selfie/character view page when the tattoo had no writing or a 'none'-type counter.
	Fixed continuity error at the start of the demon TF sex scene for Meraxis, where Meraxis would always be described during her initial vaginal penetration as being a virgin, even if you'd previously taken her virginity.
	When getting a demonic or youko sexual partner to grow a penis during sex via use of the 'Grow cock' action, their penis skin colour should now match their race, unless it's been previously set to a different colour.
	Fixed parsing issue when equipping Enforcer's night vision goggles on an NPC.
	Fixed issue where the 'strapless bodysuit' clothing would throw a background error when being equipped, and then fail to display in your inventory UI while being worn. 
	The 'spaghetti crop tank-top' clothing no longer conceals the stomach slot.
	Fixed issue which was present in several dialogues where a character who you've impregnated would act as though you'd previously reacted to their pregnancy, even if it was the first time you'd seen them pregnant.

----------------------

PATCH NOTES FOR v0.4.4.5

FriendlyAlienFriend's artwork:
	Added artwork for Leotie (Nyan's mum), in clothed, lingerie, and naked variations, each with a pregnant version.

Engine/Modding:
	Converted all groin clothing from hard-coded files to xml files (located in 'res/clothing/innoxia/groin').

Gameplay:
	Added the next section of the main quest, where you need to travel to Themiscyra to find out if it's being threatened by Lunette's daughters. (There are a few scenes marked as having placeholder dialogue. I'll get them filled in for the next update.)

Weapons:
	Added 'morning star' weapon (one-handed, sold by Vicky).
	Added 'xiphos' weapon (one-handed, only obtainable during the Themiscyra quest for now).
	
Clothing:
	Added 'fur cloak' clothing item (over-torso/neck slot, androgynous, sold by Nyan).
	Added 'nipple chain' clothing item (nipple piercing slot, androgynous, sold by Kate, two stickers to apply/remove extra chains).
	Added 'horn chains' clothing item (horn slot, androgynous, sold by Kate, two stickers to apply/remove extra chains).
	Added 'thin horn rings' clothing item (horn slot, androgynous, sold by Kate).
	Added 'ear cuff chain studs' clothing item (ear piercing slot, feminine, sold by Kate, two stickers to apply/remove extra chains).
	Added 'peplos' clothing item (torso slot, feminine, sold by Monica).
	Added 'himation' clothing item (over-torso slot, feminine, sold by Monica).
	Added 'sandals' clothing item (foot slot, androgynous, sold by Monica).
	Added 'meander ring' clothing item (finger slot, androgynous, only obtainable during the Themiscyra quest for now).
	The 'jockstrap' clothing item no longer incorrectly conceals the wearer's anus.
	
Items:
	Added 'Amazon's Secret' (sold by Ralph, applies a 24-hour effect: when orgasming during a tribbing action, there's a chance to impregnate your partner, using fertility for the impregnation calculation instead of virility).
	Added 'Amazonian Ambrosia' (only obtainable during the Themiscyra quest for now, applies +femininity and +muscle).
	
Sex:
	When having dominant sex with your elemental, your elemental is no longer able to bring an end to the sex scene.
	Characters kneeling behind or humping a partner who's on all fours can now use that partner's tail/tentacles/fingers.
	The 'lubricate fingers' and 'lubricate tail' sex actions should now always be available to you (unless physically impossible or if mouth/fingers/tail are already occupied).

Other:
	Nerfed the attribute bonuses gained from 'Lyssieth's true power' perk.
	Added 'strutter tease' and 'leg lover tease' as fetish-related tease attacks for the 'strutter' and 'leg lover' fetishes, respectively.
	Improved dialogue flow when using your elemental to intimidate the imp guards in the fortresses in Submission.
	Added a 'side braids' hair style.
	During the new 'bitch' content (where the player completely submits to a random NPC), the requirement for NPCs to have the selfish trait in order for them to take the player to be tattooed has been removed.
	Added 'shaggy' as a non-standard covering modifier to cow fur.
	The current time and date is now hidden during a bad end.

Bugs:
	Parsing fixes.
	Fixed issue where 'Lyssieth's true power' perk would not enable you to transform your demonic body parts into human parts.
	Tail and wing self-transformation options should now be populated with all intended races when using the debug menu to test the elder Lilin perks.
	When skipping the prologue at the start of a game, imported characters will now correctly gain 5000 flames on top of any flames they already had, instead of flames being set to 5000.
	Fixed bug in the rental mommy t-shirt encounters where the 'dommy' title would spawn dominant NPCs, and the 'subby' title would spawn submissive NPCs, instead of the other way around.
	Fixed bug with the rental daddy t-shirt where the 'subby' text title was assigned to the 'bottom text' sticker category instead of 'top text'.
	Unique NPCs no longer have a random chance to have the 'ahegao' perk (Takahashi is unaffected by this change).
	Fixed issue where NPCs would not be targeting their intended partner in sex scenes which used the 'preferredTarget' variable.

----------------------

PATCH NOTES FOR v0.4.4.2

FriendlyAlienFriend's artwork:
	Added new pregnant variations for Nyan's clothed, lingerie, and naked artwork.

Contributors:
	Fixed latex stocks always being referred to as black in their description. (PR#1671 by Anonymous-BCFED)
	Added a delete button to custom character images, enabling you to remove custom images without having to manually delete the image from the charatcer's 'custom' artwork folder. (PR#1637 by NoStepOnSneks)
	Fully implemented all of the Elder Lilin perk checks, which for the time being can be turned on/off via the debug menu. (PR#1631 by Maxis010)
	Removed the 'enchantmentLimit' element from all xml files, and from the Java code that parses those xmls, as support for this element was dropped in a prior enchantment update. (PR#1618 by CognitiveMist)
	Updated 'hyena_bone_crush.xml' to include damage variance, and changed links from master branch to dev branch in 'dagger.xml'. (PR#1616 by CognitiveMist)
	Added warnings for if a weighted map contains bad values. (PR#1614 by CognitiveMist)
	Adds an alarm clock function to places where you can rest: Lilaya's house room; Friendly apartment sofa; Elis tavern room; Dairy farm dormitory. (PR#1606 by CognitiveMist)
	If a random NPC attacker (in Dominion, Submission, Harpy Nests, or Elis) has the 'cum addict' fetish, or they are under the effects of an arcane storm, there is a 10% chance that they will spawn with some dirty inventory slots. (PR#1582 by CognitiveMist)
	Added sorting options to the slave list. (PR#1662 by Anonymous-BCFED)
	Changed all old FITS_HARPY_WINGS item tags to FITS_ARM_WINGS as the former is no longer supported. (PR#1663 by DSG)
	NPCs who are freed via use of a Freedom Certificate are no longer able to be re-enslaved afterwards. (PR#1649 by Maxis010)
	Fixed some sizing issues with item tooltips. (PR#1674 by Nonny5Mouse)
	Fixed incorrect parsing in tail type transformation text. (by Stadler)
	Typo fixes and fixes to descriptions in role-reversed witch altar scenes. (PR#1677 by Anonymous-BCFED)

Misc fixes contribution (PR#1664 by MintyChip):
	Added spaces before the fluid modifier descriptions in the appearance screens.
	Taurs now spawn with their race's default GenitalArrangement (e.g. alligator-taurs now have cloacas).
	Fixed the params of the method applyLegConfigurationTransformation's javadoc.
	Fixed visual bug where displayed file path for transformation presets was set to the same one as enchantments.
	Improved positioning of the infertility/fertility perks so that their connecting lines no longer appear to be connected to unrelated perks.
	Changed the octopus hair covering type to mimic the octopus skin covering type.
	Imported characters now correctly receive Lilaya's 5k flames if they skip the prologue.
	Made it so that half-demons lay eggs if their other half's race lays eggs.
	Added a 'clear alerts' button to the encyclopedia menu.
	added a 'clear stats' button when importing a character.

Slime tweaks contribution (PR#1665 by MintyChip):
	Made it so that the slime attacker's slime transformation applies the same effects as the biojuice for the sake of consistency.
	Added flavor text to the biojuice description to mention that it's "heavily processed" and thus corruptive where the source (slime queen in the bath scene) is not.
	Nerfed the permanent corruption gain from biojuice, as it seemed like a harsh effect if a new player just wandered into the submission.
	Made it so that elementals can't have their body material transformed into SLIME or FLESH using the biojuice or flesh potions.


Engine/Modding:
	Added a new element, 'bodyOverviewDescription', to tattoo xml files, which is used in the newly-added tattoo section of the character appearance page. (If missing, the basic description is used instead.)
	Converted Fetish enums to instances of AbstractFetish classes.

Gameplay:
	Added a minor expansion to Lilaya's panties content, where after threatening Rose you can gain access to a submissive threesome scene with her and Lilaya.

Items:
	Added new tattoo types: spider; rose; crossed blades; pentagram; trinity and spiral Celtic knots.

Sex:
	Hand-holding is now tagged as a 'loving' action (similar to 'Caress face', 'Kiss cheek', etc.), so NPCs will now only use this action if they do not have the sadist fetish and their affection towards their target is at least 'caring'.

Other:
	In the character appearance page, a description of the character's tattoos is now shown at the bottom.
	In the rental mommy random customer encounter, the chance for the customer to be a dom or a sub is now 60/40 based on your fetishes instead of 100/0, and 90/10 based on the writing on your tshirt instead of 100/0.
	The map screen in your phone menu now lists major maps within the selected region before all other maps.
	Bat eyes now grant the night vision ability (which negates the 'darkness' status effect).
	Siblings who are born at the same time are now defined as being twins to one another. Katherine and Kelly have now also been correctly defined as being twin sisters.
	The random NPC who spawns during the 'walkies' content for the new repeated-submission alleyway content can now spawn with a pussy instead of always spawning with a cock.
	The 'Lyssieth's power' perk now changes into 'Lyssieth's true power' after transforming into a demon, granting stronger attribute buffs.
	Added a 'begging' alternative to Amber's walkies scene to remove foot worshipping content for if foot content is turned off in your settings.
	Added a 'shoulder massage' alternative to Vanessa/Ms. Cunningham's foot massage scene to remove foot massage content for if foot content is turned off in your settings.
	Arthur's room no longer takes up one of the available rooms in Lilaya's house, and instead is now placed adjacent to the lab. (This will be retroactively applied when loading into this version if you have already placed Arthur's room.)
	Added a couple of options in the debug menu which allow you to skip Dominion and Submission quests (located on the second page of the 'Main' tab).
	While an arcane storm is raging, storm-immune NPCs who treat you as their bitch will now only use the 'fuck' option in encounters, so as to address the inconsistency of being taken to public places that were seemingly unaffected by the storm.
	Added some minor description variations for the 'seductive look' sex action (available while in the 'all fours' sex slot) for if the performer is identified as an owl-morph and has a 'raptor' race face type.
	Added ability to manage your elemental's fetishes to their management dialogue options.
	Gaining levels for fetishes now applies increased base damage to any associated tease attacks, up to a maximum of +4 at level 5. Base damage for all fetish tease attacks was reduced from 5 to 3 as part of this.
	Added a new 'Pregnancy duration' option in 'Gameplay' settings to define the length of pregnancies, with the default being 1 week and the maximum being 40 weeks.
	Scarlett's oral sex scene for the romantic setup for Helena now ends after Scarlett has orgasmed once, and you can now use the 'Skip sex' action in Helena's sex scenes.
	After completing the 'Vengar's Tyranny' side quest, the next time you enter an Enforcer Checkpoint tile in Submission while in possession of a slaver license, Claire will offer you the option of taking ownership of the four milkers from the Rat Warrens.

Bugs:
	Typo fixes and minor text improvements.
	Fixed several places in the new repeated-submission alleyway content where vagina interaction content would be used even if the player didn't have a vagina.
	Fixed issue where many racial books incorrectly had their author listed as 'Professor Webster'.
	Fixed several instances where, during Lyssieth's demon TF scenes, after starting the sex scene with the 'pussy only' action, there were references to her having a cock.
	Fixed bug where Meraxis would always be located in the tavern in Elis, even when she should have been in her citadel or in Lyssieth's palace.
	Fixed bug where tail interactions in sex scenes would not be available in some positions, such as when kneeling behind a partner in the all fours position.
	Fixed bugs with incorrectly-defined perk categories, which should fix issues with incorrect tracking of perk points when spending 'physical-only' perk points (earned from Pix's gym).
	Fixed bug where if you teleported to the lake in the Elis map, then selected 'Back', you would return to the tile from which you teleported, instead of to an adjacent fields tile.
	Sabotaging a condom no longer costs essences, and also now displays the condom's correct name in the event log.
	Fixed minor issue with configuration of several clothing items which meant that coverable areas were being incorrectly concealed. Clothing fixed: tied-up croptop; one-strap crop top; cropped tank-top; cropped T-shirt; cropped sweater.
	The exit icons in the Farmer's Market in Elis should now correctly be displayed on the map.

----------------------

PATCH NOTES FOR v0.4.4

Contributors:
	Added offspring encounters to the bat caverns. (PR#1504 by Stadler76)
	Fixed an issue where clothing management could sometimes throw a Null Pointer Exception. (by Cognitive Mist)
	Fixed issue which was causing the message 'var timer not found...' to be printed to the error log. (by Cognitive Mist)
	Fixed an issue where the AbstractSubspecies#getSubspeciesWeighting method was not working correctly, causing Subspecies weighting to fail and errors to be thrown. (by Cognitive Mist)

Engine/Modding:
	Added parser hooks for tattoo counter type, count type, and writing styles, and added a new addTattoo() method in the GameCharacter class, allowing you to add tattoos to characters and then add writing/counters to the tattoo.

Gameplay:
	Filled in all placeholder scenes for the content in the tavern, 'The Crossed Blades', and added a way to have sex with Oglix (after completing her beer-bitch barrel quest).
	Added encounter to 'Dominion street', 'Submission walkway', and 'Elis street' tiles for when wearing the 'rental mommy/daddy' t-shirts, where a member of the public will offer to pay the price displayed on your t-shirt to have sex with you. The t-shirt must not be concealed by other clothing for the encounter to trigger, and it will trigger less often when higher prices are displayed.
	Added the 'surrender' and 'Request transformation' action from Elis alleyway encounters to Dominion alleyway/demon alleyway, Harpy nest walkways, Submission tunnel, and Bat Caverns encounters.
	Expanded random encounter content in Dominion alleyways, Dominion demon tiles, Harpy Nest walkways, Submission tunnels, Bat Caverns, and Elis alleyways, by making it so that after using 'offer body' or 'surrender' actions three times, the NPC will demand that you become their bitch, after which several new options will be available upon repeat encounters.

Clothing:
	Added several more sticker variations for the 'rental mommy' and 'rental daddy' t-shirts, and allowed all colours to be chosen for the tertiary dye for the 'rental mommy' t-shirt.

Other:
	Added armpit and intercural counts to the phone menu's sex stats screen.
	Clothing stolen using the 'Steal' spell (which is currently not available to gain outside of the debug menu) now renames stolen clothing from character X following the pattern: 'clothing_name' to 'X's clothing_name'.
	The trigger for talking to Roxy about firebombs (stage 1 of the 'Spicy Meatballs' quest) no longer requires you to have asked Axel about Vengar first.
	Post-combat transformation scenes will now add/remove and alter the size of crotch-boobs.
	Slightly adjusted encounter chances in Elis's alleyways, making it slightly more likely to encounter an attacker than finding an item, prostitute, or offspring.
	Forced TF potions from alleyway attackers should now apply more drastic hair length TFs, speeding up the forced TF process.

Bugs:
	Typo fixes.
	NPCs with arm-wings who are added as beer-bitches to 'The Crossed Blades' will now correctly have a 'barrel' clothing item applied to them.
	The 'Encourage cum on X' action is now correctly disabled during armpit and intercrural sex for characters who are the one who's about to be cummed on (this is a different action to 'Request cum on X', and is intended for third party participants).
	Fixed issue where arctic wolf-morphs would correctly spawn with pale skin/white fur, but incorrectly-coloured nipples, vagina, and anus.
	Brittany (the bimbo harpy matriarch) now correctly has 'tanned' skin colour instead of 'light'.
	The 'Between legs' sex positioning action in the 'sitting' sex position is no longer available while targeting taurs (as taurs should not be able to make use of the sitting position slot).
	Fixed issue where Kruger would sometimes switch into an unsuitable sex position in his sex scene.
	Fixed background error being thrown when loading a game in which your character was in Submission.
	Fixed issues with the offspring encounters in Submission using the same dialogue as Dominion's alleyways.
	Fixed slight inconsistencies in bat cavern encounter dialogue which were referencing Submission's tunnels instead of the caves.
	Slimes who want to transform the player into a slime using forced TF will now correctly generate a slime-TF effect to apply (instead of producing a TF effect which always did nothing), then in subsequent encounters they will now generate the correct racial potions for their desired TFs.
	The transformation menu no longer displays duplicate 'Loose' buttons under orifice capacity when gape content is turned off.
	Fixed bug where skin colour preference options were not working.
	Offspring from a human mother and a human father will now randomly choose between one or the other to have their genetics based off of, instead of always choosing the father.

----------------------

PATCH NOTES FOR v0.4.3.9

Engine/Modding:
	Added 'escapeBlocked' variable to combat responses, allowing you to block the availability of the escape action during that combat scene.
	Added 'resetHour' attribute support to dialogue flags, allowing you to define the hour at which dialogue flags reset, instead of only being able to reset them at midnight.

Gameplay:
	Added 'The Crossed Blades' tavern in the alleyways of northern Elis.

Other:
	Added 'light orange' as a new body covering colour.
	Renamed 'alcoholic' fluid modifier to 'strongly alcoholic', and added a new 'alcoholic' fluid modifier, which applies intoxication at a rate 10 times slower than the old, 'strongly alcoholic' modifier.

Bugs:
	Parsing fixes.

----------------------

PATCH NOTES FOR v0.4.3.8

Contributors:
	Added expanded rat-morph lore, which is fully unlocked after reading the 'Causing Mischief' book. (by Manwhore)
	Added a .txt file guide to the Lilith's Throne root folder. (by C4MG1RL)
	Fixed bug where saving on Submission's palace entrance or palace gate tiles would cause an error to be thrown when loading. (by Maxis010)

Engine/Modding:
	Added support for defining an author name to subspecies' lore books, by defining an 'author' attribute in the 'htmlContent' element. See 'res/mods/innoxia/race/hyena/subspecies/bookEntries.xml' for an example.
	Made minor improvement to performance of status effect calculations.

Gameplay:
	Added encounters to the northern alleyways of Elis, all of which only trigger during night-time hours:
		Alleyway attackers - Same as Dominion alleyways, but with a new 'Surrender' option to apply forced TFs (if the attacker wants to TF you).
		Alleyway prostitutes - Same as Dominion alleyways.
		Item/clothing/weapon discoveries - Work the same way as in Dominion alleyways.
		Offspring discovery - Same as Dominion alleyways and Submission tunnels. These can now also be triggered by using the offspring map in the Elis alleyway tiles.

Clothing:
	Added 'nose ball stud' clothing item (nose piercing slot, androgynous, sold by Kate).

Sex:
	Made the 'Stop sex' action available during orgasm preparation to prevent an issue in large-group sex scenes, where you could get stuck in infinite orgasm-preparation loops.
	
Other:
	Added functionality to save/load self-transformation presets, in the same way that item enchantments can be saved/loaded.
	Added skin colour content preference, which can be adjusted at the bottom of the 'Content options -> Body' menu.
	Moved Gender, Orientation, Age, Furry, and Fetish preferences from the 'Options' screen to the 'Content options' screen.
	Added 'orange' to available penis and skin colours.
	Added dialogue variation for if Lyssieth takes the player's vaginal or anal virginity.
	Callie's opening hours have been changed; her bakery is now open from 9:00-15:00, which increases to 07:00-17:00 after you've donated enough to upgrade her store.
	Altered squirrel-morph's racial bonus from +1 health shielding to +5 physique and +10 critical damage.
	Youko offspring can no longer be found in Dominion's alleyways, and can instead be found in Elis's alleyways (until the Shinrin Highlands content is added, then they'll be moved there).
	Added 'pronged' antlers as a new generic horn type, which can now be a default horn type for newly-spawned demons.

Bugs:
	Parsing and typo fixes.
	The 'Loving confession' and 'Loving response' sex actions now correctly have a associated corruption values of 'pure' instead of 'dirty'.
	Demons with a 'martuilani' surname ending (identifying them as a direct daughter of a lilin) now have their offspring generated with the surname ending 'martu' (meaning a descendant of a lilin) instead of 'martuilani'.
	Fixed issue where in some circumstances the player character was incorrectly being detected as being related to Lyssieth and Meraxis.
	Fixed bug where combat responses defined in external xml files would try to parse their title and tooltip before the game had started, causing background errors to be thrown.
	Fixed issue where Dominion prostitutes would not be removed from their tile after beating the player while noncon content was turned off.
	Fixed bug in sex scenes with unique stop sex conditions for NPC, where the unique stop conditions would not be used after changing position.
	Fixed background errors being thrown when background sex calculations were being performed (such as when two slaves would have sex with one another).

----------------------

PATCH NOTES FOR v0.4.3.5

AceXP's content contributions:
	Added more sex actions in each of the harpy matriarch's nests, which are available after having pacified those nests (as part of the 'Angry harpies' side quest).
	Added a new area, 'Lilaya's Dungeon', beneath Lilaya's mansion. You can access this area from reading the 'People as Property' book in the mansion's library, which unlocks after obtaining Lilaya's recommendation for a slaver license.

Contributors:
	Fixed issue where the Innoxia's Gift debug item wouldn't work correctly. (by AceXP)
	Added a new 'Strapless bodysuit' clothing item, which is sold by Nyan/Monica. (by C4MG1RL)
	Added support for dynamically-resizing action tooltips. (PR#1617 by CognitiveMist)
	Added three new clothing items: 'Round sunglasses' (unisex), 'Heart sunglasses' (unisex), and 'Cat-Eye sunglasses' (feminine, supports patterns), all of which are sold by Nyan. (PR#1613 by CognitiveMist)
	Added several additional entries to the parser namespace, giving modders handles to nine more gameplay-relevant classes. (PR#1611 by CognitiveMist)

Engine/Modding:
	Added support to define pre-lubed areas at the start of sex via a new 'startingLubrications' element in external sex managers (see 'res/sex/innoxia/managers/meraxis/duel/masturbation.xml' for a commented example).
	Added catch for passing in a null character argument for the setNippleSize(), setNippleShape(), setAreolaeSize(), and setAreolaeShape() methods, making it safe to call these methods with a null character in modded race's 'applyRaceChanges' and 'applySubspeciesChanges' elements.
	For race modding, support has been added for defining lip names and descriptors in mouth type xml files (see 'res/mods/innoxia/race/hyena/bodyParts/mouth.xml' for a commented example).
	Added support to mod in 'Loving confession' and 'Loving response' lines to sex managers in the same way that submissive and rough lines can be added (see 'res/sex/innoxia/managers/meraxis/duel/masturbation.xml' for a commented example).
	Moved more dialogue out of hard-coded Lilaya's lab and library classes into external xml dialogue files.

Gameplay:
	Added 'Ahegao' as a new trait (located in the lust tree), which grants +15% lust damage, -5 lust shielding, and adds an extra paragraph to orgasm descriptions.

Clothing:
	Added sticker support for the 'lowback bodysuit' clothing item, allowing you to remove/attach the shoulder straps.

Sex:
	ONGOING SexActionTypes are now available for immobilised characters to use during sex, but only so long as the action's performing areas doesn't include a virginity-taking penetration type.
	The 'Cocoon', 'Tentacle restraint', and 'Constrict' immobilisation sex actions are now used by dominant-sex-slot NPCs who have the 'bondage applier' fetish, instead of requiring dominant, sadist, and non-con fetishes.
	Ball-focused sex actions are no longer available if the targeted character has a dildo instead of a real penis.
	NPCs will now only use the 'Request facial' orgasm preparation sex action if they have a positive desire towards the 'cum addict' fetish and if the person orgasming has a penis.
	Added 'Kiss cheek' and 'Caress cheek' as gentle-paced counterparts to the sadistic 'Spit in face' and 'Slap face' actions. NPCs who are using the gentle pace, who lack the sadist fetish, and who have 50+ affection towards the target will use these actions.
	Added 'Loving confession' and 'Loving response' sex actions, which again are used only by NPCs who are using the gentle pace, who lack the sadist fetish, and who have 50+ affection towards the target. 'Loving response' is only ever used as an immediate response to 'Loving confession'.
	Added 'Hand holding' as a new ongoing action type.
	The 'Encourage creampie' and 'Request creampie' actions can now be used when the orgasming character is penetrating nipples, crotch-nipples, and urethras.
	Added 'Encourage knot' and 'Request knot' orgasm preparation actions for when the orgasming character has a knotted penis, which result in the orgasming character using the 'Knot them' action instead of 'Creampie them' (so long as the orgasming character is not ignoring requests).
	Added NPC reaction to a creampie or knotting request to let you know if they're willing to do as you ask or not.
	Orgasming characters no longer require a penis to have their orgasm description start with a small sentence describing the orgasming character's position.
	NPCs are now able to use immobilisation-related 'struggle' actions while in the resisting sex pace.

Other:
	Yui's anilingus scene now correctly starts with her asshole lubed by her girlcum, as the scne's intro describes.
	If playing on a difficulty level which causes NPCs to always match your level, their true level is now shown in brackets after their matched level in the tooltip when hovering over their name.
	Added a 'half-demon' option to the 'spawn attacker' function of the debug menu.
	Added a 'demonic-owl' eye type, which enables owl-morphs to spawn as half-demons.
	Masturbating no longer counts as the masturbating character having had sex with a unique sex partner. (So in the phone's sex stats screen, masturbating will no longer count towards the 'You have had sex with a total of X different people' tracker.)
	Added dialogue variation of first post-sex essence absorption for if the player is a spectator instead of an active sex participant.
	Callie now has the 'sterile' perk to prevent her from impregnating the player (will be reverted later when Callie impregnation content is added).
	Raptor and harpy 'lips' are now referred to as a 'beak-lips'. (There isn't a perfect solution to lip parsing for beaks, so while 'beak-lips' is quite clumsy, it's the best that I can do to help differentiate beaks from normal mouths in sex actions.)
	Added +5% lust damage to the 'Nymphomaniac' trait.
	Added small offspring encounter dialogue variations for if the player was the offspring's incubator.
	Added icon indication on sex-start actions for if the sex will involved non-con.
	Set reindeer-morphs to have an extremely low chance to spawn in Dominion, which enables your reindeer offspring to be encountered in Dominion's alleyways.
	NPCs who use fetish-altering potions will now generate potions that can alter penis, lactation, and foot related fetishes (provided the relevant lactation and foot content toggles are turned on).

Bugs:
	Typo and parsing fixes.
	The ring gag clothing item now uses the correct icon, instead of displaying the ball gag icon.
	Fixed issue where you could still use the 'fly' fast travel option even if the map was supposed to not allow flying (such as in Evelyx's Dairy, among many other internal locations).
	Maps which are located in the Foloi Fields (such as Evelyx's Dairy) are now displayed under the 'Elis' map tab in your phone's maps screen, instead of in the 'Dominion' tab.
	Fixed issue where the 'Ball gag demo' action at Yui's stall (in the Farmer's Market at Elis) would not work and throw potentially game-breaking background errors.
	Fixed issue where wolf-morphs could spawn with white fur, inadvertently making them arctic wolf-morphs.
	Fixed bug where using Penelope's cosmetics services would sometimes incorrectly use a character other than the player to apply cosmetics changes to.
	Offspring who had both a father and mother that weren't the player, but were incubated by the player, are now correctly detected as being available to find via the offspring map or randomly in suitable tiles.
	Fixed issue where dialogue flow would break during Enforcer encounters while wearing an Enforcer set and being in possession of the contractor pass.
	Characters no longer regain their anal virginity upon transforming their lower body type (such as into a taur or lamia).
	Characters who are unable to orgasm due to enchantment effects will no longer have orgasm effects applied from using the 'Quick sex' action.
	The description for the tagged choker clothing item now correctly lists the top text first and then the bottom text afterwards.
	Fixed issue with Callie spawning with incorrect skin/hair colours.
	You can no longer enter Callie's bakery, 'The Creamy Bakey', on Sundays, when it's meant to be shut.
	Fixed issue where selecting the 'Buyback' action throwing background errors and softlocking the game if there were no items available to buy back.
	Eagle and bald-eagle morphs should no longer spawn in with huge height values.
	Fixed issue where you could go back to the Rat Warrens and enter it if you went there after defeating Vengar in combat but before handing in the quest to Axel.
	Selling items to Fae, Heather, and Kazik (in the Farmer's Market in Elis) no longer gives you Faire Tickets.
	Fixed issue where if character1 was being forced to cum inside character2 during the same turn that character3 was also orgasming, then character1 would sometimes incorrectly be treated as orgasming inside character3.
	Fixed issue where the 'Service ass' action which was displayed after flirting with Astrapi wasn't working.
	Using the 'Quick sex' action will no longer result in characters being able to perform actions which should have been prevented due to limits on available positions or positioning slots.
	Fixed issue with incorrect dialogue flow in several parts of Lilaya's lab.
	
----------------------

PATCH NOTES FOR v0.4.3.1

AceXP's content contributions:
	Added a scene for watching Lilaya and Rose have sex in Lilaya's lab.
	Added repeatable sex content for Angel, which is unlocked after visiting her after purchasing a prostitution license.

Nnxx's content contribution:
	Added a bakery in the north-west of Dominion, called 'The Creamy Bakey'.
	Added a new horse-girl character, Callie, who runs this shop, and added some sex content for her.
	Added three new doughnut food items which can be purchased from Callie.

Contributors:
	Fixed issue where newly generated offspring would be of a random subspecies if they were meant to be a half-demon. (by AceXP)
	Fixed issue where sometimes starting lust would be zero for newly spawned encounters instead of at their resting lust level. (by AceXP)
	Fixed bug where if a character was immobilised then no orgasm options would be available for them to choose from, which led to a blank action grid being displayed to the immobilised player when a character reached orgasm. (PR#1638 by miome)
	Added support for instantiating all NPC classes via the addNPC(String npcGenerationId, String parserTarget) method by using predefined names (like FieldsBandit) or qualified names (like dominion.DominionAlleywayAttacker). Also updated the default (no parameter) NPC constructors to make use of gender preferences. (PR#1615 by AceXP)
	Fixed issue where offspring subspecies names weren't being generated correctly, fixed issue where offspring between demons and non-demons were not being generated as the correct subspecies, and added previously unused dialogue for all calendar months in the player's room. (PR#1634 by AceXP)
	Fixed issue where a player wearing the correct patrol uniform would auto-fail the uniform check during Enforcer alleyway encounters. (PR#1635 by DSG)
	Maxis010's bugfix PR#1630:
		Default penis and vagina values should now always respect the default values drawn from the character's race upon generation.
		Event log entries are now capped at 50 to address a potential memory leak issue.
		Stopped gear resealing onto the character upon loading if it had already been unsealed.
		Multiple dialog & tooltip fixes (with contribution from Phlarx).
		Moved QUEST rarity clothing checks to banishNPC method as previously calling it in the unequipClothingIntoVoid method was causing a duplication bug.
		Changed all removeNPC method calls to banishNPC method calls so that all NPC removal checks are applied.
		If the player's offspring are being incubated in an NPC which is removed, then the offspring are no longer deleted.
	
Gameplay:
	Filled in all placeholder dialogue in Penelope's spa, 'Woolly Heaven'.
	
Other:
	The succubus/incubus attackers in Dominion's alleyways now draw on your gender preferences to generate their gender, instead of always being either male or female.
	
Bugs:
	Parsing fixes.
	Corrected imp lore description incorrectly stating that imps could not self-transform.
	Fixed issue where externally-defined sex managers would throw errors if a preference returned an empty String.
	
----------------------

PATCH NOTES FOR v0.4.2.9

Contributors:
	Fixed issue where offspring from demons and non-demons were being generated as the wrong subspecies. (by AceXP)
	Added 'equipClothingFromOutfitId()' method to CharacterUtils.java, making it easier to equip outfits on npcs in xml files via calls to game.getCharacterUtils().equipClothingFromOutfitId(). (by AceXP)

Engine/Modding:
	Converted all hard-coded BDSM-set, stomach-slot, and 'women's fashionable leather jacket' clothing files to external xml files.
	Fixed incorrect documentation for the 'sexClothingEquippable' attribute in the commented sex manager, 'meraxis/duel/masturbation.xml'. (This variable defines whether or not the character can equip sex toys on others, while the old, incorrect documentation stated that it defined whether the character could have toys equipped on them.)
	Added 'clothing' and 'npc' parsing targets for the 'sexClothingEquippable' attribute in xml-defined sex managers.
	Added 'ROPE' and 'CHAINS' as new immobilisation types (in ImmobilisationType.enum) for use during sex, along with associated status effects.

Gameplay:
	Added sex content for Penelope's spa 'Woolly Heaven', which can be found in Elis's shopping precinct. (There's still some placeholder dialogue in Penelope's scenes, which will be filled in for the next update.)
	Added 'arctic-wolf-morph' as a subspecies of the wolf-morph race. (To be classified as an arctic-wolf-morph, be detected as a wolf-morph and have white fur.)

Clothing:
	The 'wrist restraints' clothing item from the BDSM set can now be equipped to the ankle slot in addition to the wrists slot.
	Added stickers to the 'tagged choker' BDSM clothing item to allow you to customise the text on the tag.
	Added secondary dye colours to 'overbust corset' and 'underbust corset', and secondary and tertiary dye colours to 'fashionable women's leather jacket'.

Sex:
	You can now equip condoms onto unique NPCs in most of their sex scenes. (A few special sex scenes prevent this behaviour, such as Lyssieth's demon TF sex scenes.)
	Condoms can now be equipped onto a character's penis even if their penis is involved in an ongoing action, so you no longer need to stop ongoing action, apply condom, then restart the action.
	NPCs now remove condoms that were equipped during sex when sex ends.
	All speech actions are now available while being immobilised in sex scenes for both the player and NPCs.

Other:
	The 'Random race transformation' potion effect (added via enchanting food with 'core' + 'transformative I' modifiers) no longer tries to apply transformations which have already been applied to the target, so potions with 16 of these effects will now always fully transform a target into the potion's race.
	'Woolly heaven' is no longer closed during weekends.
	Standardised hyphenations in the names of several subspecies.

Bugs:
	Added missing sex actions for the 'humping' sex slot while in the 'over desk' sex position.
	Fixed issue where you could have vaginal sex with Kazik even if you had no vagina.
	Fixed issue where in some sex scenes you could swap positions with a character who should have been blocked from accessing your position.
	Fixed the 'orgasmCumTarget' element in sex managers not working correctly and throwing background errors.
	
----------------------

PATCH NOTES FOR v0.4.2.5

Contributors:
	Fixed issue where characters without vaginas would spawn with the pure virgin fetish. (by Maxis)
	Implemented new way of handling offspring who haven't yet been met, significantly improving turn time performance and save file size in games in which you have a lot of unmet offspring. (PR#1622 by AceXP)

Engine/Modding:
	Added new BodyPartTag values 'TAIL_ATTACK' and 'TAIL_VENOMOUS_STING' for future use in bee/scorpion/etc. tails.
	Added several 'CAFFEINATED_' ItemTags for use in defining consumable items as being caffeinated (so that they can apply intoxication effects to spider-morphs).

Gameplay:
	Added characters and basic trading actions for the last remaining shops in Elis's shopping precint, Wall's End. (More content for each store will be added later.)
	Added a new 'raptor' race which includes the subspecies: falcons (default); eagles; bald eagles (converted from harpy race); and owls.
	Added 'Raptor energy drink' and 'Raptor energy bar' as new drink and food items for the new raptor race.
	Added a new 'mouse' race which includes just one 'mouse' subspecies.
	Added 'Harvest Mouse's barley water' and 'Harvest Mouse's cheese' as new drink and food items for the new mouse race.

Clothing:
	Added 'safety glasses' (scientist set, eye slot, androgynous, sold by Nyan).

Sex:
	NPCs will now only use the orgasm denial action during sex if they have the orgasm denial fetish. (Previously, all that they needed was to have a positive desire towards that fetish.)

Other:
	Changed references to beer and cider bottles to being on tap in the two pubs in Elis.
	Changed Mintallys's Sunday milk flavour/theme from grape/purple to cherry/red.
	Gave Amber a lore-friendly demonic surname.
	Lyssieth's dominant and submissive sex options are no longer tied to her using her pussy or growing a cock, and instead you can request that she use her pussy or grow her cock for both dominant and submissive sex scenes.

Bugs:
	Parsing fixes.
	Fixed issue where you could use orgasmic level drain during bad end sex scenes.
	Fixed (harmless) background errors being thrown when starting a new game, caused by failing to parse vagina types before the game had fully initialised.
	Your offspring who have been incubated by someone else are now correctly counted as part of the 'Total offspring' count in the phone menu's pregnancy stats screen.
	Fixed issue where you could ask Dale about Monica's milker before even having started Monica's quest.
	Fixed issue with several attributes in xml-defined responses (such as for fetish/perk requirements, sex, combat, and trading), where the first definition of these attributes would be used for all subsequent responses.

----------------------

PATCH NOTES FOR v0.4.2.3

Contributors:
	Fixed bug where clothing stickers weren't transferring when enchanting clothing. (by CognitiveMist)
	Fixed issue where the error log would generate the entry 'Warning: Parser target of X has been replaced!' when randomly-generated NPCs were getting removed. (by AceXP)
	Prevented a null exception when a move had zero equip-weight. (PR#1596 by CognitiveMist)
	Fixed several bugs and updated modding information for patterns. (PR#1605 by CognitiveMist)
	Fixed rare bug when importing clothing which would sometimes result in modded clothing not showing up for sale. (PR#1607 by CognitiveMist)
	Adjusted NPCs' reference to their working hours to respect the 12 or 24-hour preference in the player's settings. (PR#1609 by CognitiveMist)
	In the self-transform menu, the comparators used for sorting horns and wings have had inconsistencies fixed. (PR#1610 by CognitiveMist)
	Improved Encounter generation code, improving performance in Lilaya's Home and Dominion tiles. (by AceXP)
	Fixed incorrect descriptions related to incubation stats in the character information page. (by AceXP)
	Fixed issue where the 'quick sex' action would perform blocked sex types. Also fixed parsing issues with paizuri tooltip and the naming of horse vaginas. (PR#1619 by Maxis010)

Assorted Bugfixes Contributed by Maxis010 (PR#1603):
	Fixed typos both in dialogue and code.
	Fixed issue where artwork could become invalid after a character was transformed (which was what was causing errors when removing Scarlett's penis).
	Fixed bug where Ashley would be set to be friendly towards herself instead of towards Nyan.
	Improved detection and removal of danger characters in save game file names.
	Added missing check for body hair content setting.
	Fixed issue with the saving/loading of enchantments sometimes loading incorrect enchantments.

Engine/Modding:
	Slightly improved performance of encounter generation.
	Added support for 'one-shot' weapons (intended primarily for thrown weapons), which causes the weapon to be removed from the player after being used. You can define chances to recover the weapon at the end of the turn and at the end of combat. See the 'res/weapons/innoxia/dagger/dagger.xml' for comments on how to define a one-shot weapon.
	Added a 'attackDescriptionPrefix' element to weapon xml files, allowing you to define a more suitable attack description to fit the sentence 'X your enemy for N damage!'. See the same dagger file mentioned above for a commented example. If the element is not found, then the 'attackDescriptor' element is used instead (so there's no real need to refactor any mods).
	Added a new TFModifier value 'ENCHANTMENT_LIMIT', which acts like any other attribute boosting TFModifier (to increase the wearer's enchantment capacity) when selected as the secondary TFModifier to a primary 'CLOTHING_MAJOR_ATTRIBUTE' TFModifier. This cannot be selected by the player in-game (for balance reasons), and so is only for if you want special modded clothing or weapons to add enchantment capacity.
	Added 'SEX_PACE_' as a parser prefix hook to the SexPace enum values.

Gameplay:
	Filled in all placeholders for Evelyx's Dairy content, including the bad end there.
	If you attack Enforcers and are then defeated by them, they will now search you in the post-combat scene and confiscate any illegal items you're carrying.

Items:
	Added 'tennis ball' and 'ball of yarn' as ranged, one-shot, silly mode weapons, both sold by Ralph. (They will appear in his inventory after he restocks at midnight, and will only appear if you have silly mode turned on.)
	Converted the 'arcane firebomb' item to use the new one-shot weapon mechanic, and made it one-handed.

Sex:
	Added breasts-to-mouth actions for the interaction between the 'sitting' and 'sitting in lap' sex slots.
	Added 'Stop rape-play' and 'Allow rape-play' actions for when you're a dominant in sex and your partner is resisting due to having the 'unwilling fuck-toy' fetish, which prevents/permits them from optionally using the resisting pace (they can still resist if not enjoying sex or if they're a friendly NPC who's been betrayed by you).
	The choice of which ongoing action to reference in dirty talk lines is no longer completely random, and is now instead based on the character's fetish desire towards each ongoing action (with liked actions having more weight to be referenced).
	NPCs now have the option to reposition during sex in the 'sitting' position.
	Slightly improved the starting description and added initial actions for Kruger's sex scene, and thanks to the change above, he should now correctly switch position so as to progress from oral to penetrative sex during the scene.
	Foreplay should now last longer than 1 or 2 turns. Changes related to this: initial ongoing actions do not apply arousal gains before the first turn; arousal gains are halved while in foreplay; added this information to the arousal attribute tooltip.
	NPCs will no longer choose 'self-breast-to-finger' or 'self-breast-to-tongue' preferences for sex if they are masculine with no breasts and no positive desire towards the self-breast fetish.
	The 'Cum on feet' orgasm action is no longer available if the targeted character does not have feet (such a lamia).
	If an NPC is dominant or has equal control in a sex scene then they will no longer allow you to equip sex toys on them.
	Dominant NPCs who have orgasmed at least 2 times more than they need to be satisfied will now want to end sex if their submissive partner is still at 0 orgasms and is not aroused.
	NPCs now have the same chance to request a facial as they do to request nothing, which should stop them from almost always requesting a facial when the position allowed it.
	The 'Thrust into mouth' and 'Paizuri into mouth' sex actions will no longer be used by NPCs who have a negative desire towards receiving or giving oral, respectively.

Other:
	Changed some perks to traits and vice versa based on the concept that the only perks which should be classified as traits are the ones which you might want to disable, so:
	Perks -> Traits: Beserk, Object of desire; Irresistable appeals; Aura shielding.
	Traits -> Perks: Martial artist; Ferocious warrior; Pure thoughts; Lustpyre; Arcane precision; Arcane combatant.
	The Enforcers in the Dominion alleyway Enforcer encounters now end the 'strip' sex scenes once they're satisfied, instead of keeping on going until the player is satisfied too.
	Automatically-generated clothing name postfixes now prioritise 'of sealing' over generic positive enchantment effects.
	While they will still always spawn in as feminine or androgynous, the gender of harpies which spawn in the Harpy Nests now takes into account your gender preferences (thereby allowing futa/herm harpies to spawn up there now).
	Added a 'Defaults' button to the orientation preferences screen, allowing you to reset orientation ratios to tehir default values.
	Buffed pegasus-morph racial bonus by increasing their critical damage from 10 to 30, and altered their racial bonus's description to reference this.
	Battle axes, dories, and recurve bows now spawn with some basic enchantments.
	Weapons defined as 'common' now automatically use the same rarity calculation as clothing, so a weapon which is part of a set is defined as 'epic', a weapon with more than one enchantment is 'rare', a weapon with one enchantment is 'uncommon', and unenchanted weapons as 'common'.
	The weapons 'feather duster' and 'witch's broom' are now respectively part of the 'hard-working maid' and 'witch' sets.
	Set several weapons to 'common' rarity so that they now use the automatic rarity assignment system described above.
	Randomly-generated, non-greater NPCs now have a random skin colour (so lesser morphs with set fur colours, such as raccoon-morphs, can now spawn with a variety of skin colours instead of the same one every time, which was being based on their fur colour).
	Male spider-morphs now spawn as being masculine instead of androgynous.

Bugs:
	Formatting, typo, and parsing fixes.
	Fixed issue where the artwork would not update for Kay after feminising him.
	Fixed background error sometimes being thrown when teleporting out of Submission.
	If a tile has multiple possible encounters assigned to it, the encounter chosen is now correctly weighted based on each encounter's total chance to be selected, instead of completely randomly (which was causing issues with encounters not triggering as expected).
	The 'Impish Fiends' and 'Centaurs & More' books will now correctly unlock in Lilaya's library after having read them.
	Fixed issue where NPCs were being affected by the 3-year time skip at the start of new games, making them 3 years older than intended. This fix has been retroactively applied to all unique NPCs, so when loading into this version unique NPCs will all be 3 years younger.
	The player character now suffers from menopause at age 55 instead of NPCs' usual 52, to take into account the 3-year timeskip.
	Fixed issue where the 'Push her' sex action during Meraxis's handjob scene would show a 'No suitable description found for this action!' error.
	Fixed background errors being thrown when accessing Kate's 'Makeup' and 'Other' actions.
	If you have multiple arm rows, the action name for main and offhand strikes will no longer omit some of the attacks which are to be performed.
	Fixed bug where weapon equip requirements were not being taken into account when equipping weapons directly from the ground.
	Fixed issue where ferals could have their leg configuration transformed. (Ferals are not in the game yet, but there will be content for them added 'soon'.)
	The game now correctly saves the description of virginity losses even if the virginity-taking character is removed from the game, meaning that from now on you should no longer see the 'You lost your virginity to someone you can't remember' message. (This fix does not apply retroactively, so if you are already seeing that message, it is too late to be fixed.)
	Fixed issue where NPCs' forced-TF potions would not completely take into account the 'Forced TF Racial Limits' content setting.
	NPCs' forced-TF potions will no longer enter a state where they flip-flop between shortening and lengthening hair each time they're generated/used after combat.
	Fixed issue where demonic spider-morphs would have incorrect names when possessing the 'arachnid' leg configuration.
	Equipped clothing descriptions will now correctly be parsed according to who is wearing it.
	Armpits will no longer be described as 'hairy' if the character has no underarm air or if body hair content is turned off.
	Fixed issue with the panther-morph race, where applying smooth spotted fur to a panther-morph would throw an error and detect the character as a human.
	Slimes will no longer spawn wearing makeup.
	Removing a character's vagina no longer displays text stating that the character 'now gives birth to live young'.
	Fixed issues with Natalya's sex scenes and the centaur sex scenes related to Dominion Express never ending without the use of the 'Quick sex' action.
	The tooltips for the 'swollen belly/breasts/spinneret' status effects now correctly list all of the fluid types which are causing the inflation, instead of always referring to them as 'cum'.
	Fixed issue where when setting your elemental's name, the game would detect keys being pressed as activating their usual hotkey while trying to type in a new name.
	Fixed issue where you could start but never stop self-fingering and self-tail-to-nipple-penetration ongoing sex actions.
	The 'Explore' action in Dominion's alleyways, the Harpy Nests, and elsewhere, should no longer rarely do nothing upon use.
	The 'Cow-girl (greater)' reward offered to you in Evelyx's Dairy will now correctly transform your character's horn type.
	Evelyx's Bad End no longer gets bugged and stuck at the 'Mounted' action.
	Fixed issue in Monica's quest where if you refused Evelyx's offers during her meeting, you the option to have another meeting with Evelyx wouldn't appear, preventing you from progressing the quest.
	Random TF potions based on races which lack horns, tails, wings, or crotch-boobs will now correctly remove those body parts instead of growing generic ones.
	Fixed issue where some types of taur (such as cattle-morph taurs) were always being referred to by their masculine name even if the character was feminine.
	The 'Total offspring' count in the phone's 'Pregnancy Stats' screen now correctly includes offspring birthed from implanted eggs.
	Characters who lack feet (such as lamia) or arms (such as feral snakes) will no longer be described as having toenail or fingernail polish.
	Fixed a (harmless?) series of background errors sometimes being thrown when loading a game (which was being caused by trying to generate encounter types before the game had been fully initialised).
	Half-demon attackers in Dominion's alleyways will no longer spawn wearing completely random outfits.
	NPCs who forcibly transform you after defeating you in combat will now correctly transform your leg type to their preference before trying to transform your leg configuration.
	Characters with a rear-facing cloaca will no longer have access to their vagina and penis blocked by wearing a buttplug.
	Fixed issue where Enforcers with leg configurations of 'serpent-tailed' or 'arachnid' would spawn wearing random clothing instead of an Enforcer uniform.

----------------------

PATCH NOTES FOR v0.4.2

Engine/Modding:
	Added parser hooks for orifice capacity, depth, elasticity, and plasticity, under the respective prefixes: 'CAPACITY_'; 'DEPTH_'; 'ELASTICITY_'; 'PLASTICITY_'.
	Added 'MONTH_' parser hook for Java's Month enum, and a getMonth() method in the Game class for obtaining the current month.
	The 'orgasmBehaviour' element in sex manager files now accepts logic and is parsed on every check.

Artwork:
	Added 7 images for Kay (4 as default, 3 for when he's been feminised), drawn by Jam (https://twitter.com/JamDrawers).
	Added 2 images for Elizabeth, drawn by KT80 (https://twitter.com/KT80AT).

Gameplay:
	Filled in all placeholders for Monica's quest (who is the shopkeeper for the clothing store in Elis's shopping precinct, 'The Fashionable Moo').
	Added a 'headless horseman' encounter to the Foloi Fields (only triggers during the in-game month of October).

Other:
	Added 'dark orange' as a covering colour for body parts.

Bugs:
	Parsing fixes.
	Fixed issue with missing 'WON_SEX_NOTHING' dialogue in one of Mreaxis's duel scenes.
	The lilin book lore text is no longer shown at the end of the 'World' dialogue when talking to Lyssieth in her initial meeting scenes.
	Fixed issue where after turning down Evelyx's promotion, you couldn't repeat it the next day.
	Characters who have the sadist fetish will no longer agree to be gentle in sex (which was mainly affecting Amber's and Rose's sex scenes).
	Fixed background error being thrown when generic sex effects were being calculated where a null partner was being treated as being exposed to addictive fluids.
	Fixed parsing error being thrown if you encountered bandits in the Foloi Fields and didn't have enough money to offer them to skip the encounter.

----------------------

PATCH NOTES FOR v0.4.1.5

Contributors:
	Added Felicia (Arthur's neighbour) as a unique character who can be met after completing the first stage of the main quest (more content for her will be added later). (by Rick Docket and DSG)
	Added samoyed-morph subspecies to the dog-morph race. (by DSG)
	Added a new fetish preference menu to the options menu, which allows you to set values for influencing the fetishes and desires random NPCs will be generated with. (PR#1553 by Maxis)
	Prevented patch notes from being run through the parsing engine, which was occasionally causing null pointer exceptions. (PR#1567 by Stadler76)
	Removed the hasSexCountWith() method and replaced all of its uses with the getTotalTimesHadSex() method to fix issues with inconsistencies in dialogues. (PR#1568 by AceXP)
	Added a new setting for outfit files which makes it possible to apply an outfit to an entire region (i.e. collection of world types). (PR#1569 by AceXP)
	Created a new character class for slaves which can be bought in Slaver Alley, thereby fixing an issue where slaves generated while the player was not in Dominion/Submission would be of unexpected race types. (PR#1570 by AceXP)
	Removed unnecessary copy when accessing the unique item count of an inventory, greatly reducing inventory lag and load on the garbage collector. (PR#1573 by AtelierAmber)
	NPCs will no longer perform orgasm reactions or denials in response to the player orgasming when the player is hidden. (PR#1578 by AceXP)
	If a corruptive action is bypassed by fetish, the pink '!' icon will now be recoloured to grey to signify that no corruption will be gained. (PR#1583 by CognitiveMist)
	When the player does not have enough flames to use 'Buy (All)', but has enough to buy at least one item, the game will now offer 'Buy (Max NN)' in the 'Buy (All)' slot, where NN is the amount that will be purchased. (PR#1584 by CognitiveMist)
	Fixed issue where characters that the player had never met were getting added to the contact list when loading a game. (by AceXP)
	Fixed soft lock with the fields bandit encounter where if the bandit was willing to rape but not attracted to the player, no dialogue options would be given to continue the scene. (by AceXP)
	Fixed an rare stack overflow error when loading a saved game in which the player had slaves or followers. (PR#1590 by Jtecx and CognitiveMist)
	
Engine/Modding:
	Hair types now have a 'neckFluffChance' value to determine how likely they are to spawn with neck fluff (see the hyena's hair.xml file for a modding example).

Artwork:
	Added artwork for Catherine (the Slime Queen), drawn by Jam (https://twitter.com/JamDrawers).

Gameplay:
	Added the next stage of the main quest, where you meet Minotallys.

Body:
	Added 'neck hair/fur' as a purely cosmetic transformation tied to a character's hair, which can be applied via potion or clothing TFs.
	Chances to spawn with neck fur are: 25% for greater fox and wolf morphs, 100% for male lion morphs, 10% for greater female rabbit-morphs.

Clothing:
	Added 'heavy gemstone ring' (finger slot, unisex, sold by Nyan). Also limited the default colours that these rings can spawn in with.

Other:
	Added a 'Vestigial Multi-breast' content setting to the 'Body' category (on by default), which affects whether multiple rows of breasts are described as being 'vestigial' or 'one cup size smaller than the one above' in size.
	Increased level of fields bandits from 5-10 to 10-20.
	Added ability to reset your elemental's perks. (Action appears when viewing their perk screen.)

Bugs:
	Parsing fixes.
	Fixed bug where characters without hair could still be targeted for the 'Twintail pull' sex action.
	Fixed bug in the 'Rogue Enforcer' quest, where completing the quest would sometimes lock you in a travel-disabled dialogue screen with no responses to choose from.
	Fixed bug where some sex scenes with Scarlett, such as those encountered during Helena's romance quest, would never come to an end.
	Bandits in the Foloi Fields will no longer remain on their tile if you escape from combat against them. Any bandits which have persisted on these tiles will be removed from your game upon loading into this version.
	The racial transformative effects of the items from the three harpy bosses (the lollipops and perfume) will no longer work on characters whose race is immune to racial transformations.
	Takahashi is now added to your phone's contacts list after meeting her. (She ill be added to your contacts when loading into this version if you are past the 'Destination Elis' section of the main quest.)
	Fixed bug where the first stage of the status effect for wearing chastity clothing ('Forced chastity (calm)') would not be removed when removing the chastity clothing.
	When encountering an Enforcer patrol, the actions to be searched will no longer incorrectly be coloured red and reference having your items confiscated if you are in possession of Elle's or Wes's contractor pass.
	Elementals will no longer reset their inventories at the turn of midnight every day.
	The player character's elemental will no longer have their level scaled to a higher value based on the game's difficulty.
	Fixed issue where you could give your elemental infinite perks, and fixed a related issue where your elemental's perk screen was showing that they had 2 perk points available for the physical and arcane categories.
	The 'Thigh squeeze' orgasm action can no longer be used by characters who don't have legs.
	Fixed issue where Jhortax and Fyrsia would both be missing their weapons when (and if) you fought them in Meraxis's citadel.
	Fixed issue where bandits in the fields were always being generated as females.
	Dragon Draft consumables now restore the percentage of total health and aura which their tooltips say they will.
	Fixed issue with NPCs' descriptions not being updated after freeing them from slavery.
	Fixed issue where if you had companions enabled and started sex with one while there were NPCs present in the tile, the NPCs would be added as submissive spectators who could then be brought into the sex scene.

----------------------

PATCH NOTES FOR v0.4.1.1

Contributors:
	Fixed issue where altering vaginal urethra plasticity was affecting penis urethra plasticity instead. (by Maxis)
	Fixed bug where clothing replacements after sex would sometimes break if the clothing being replaced was of a type that was previously equipped to multiple slots. (by Maxis and deboucher)

Engine/Modding:
	Added 'deskName' as a definable attribute within external 'worldType', 'placeType', and 'sexManager' files, which functions in the same way as 'wallName', allowing you to define the name of the 'desk' used in sex scenes.
	Fixed issue where modded world types had '_worldType' appended to the end of their ids.
	Added 'canRemoveClothingSeals' as an attribute in externally-defined sex managers to prevent characters from being able to unseal clothing during that scene.

Artwork:
	Added FriendlyAlienFriend's artwork of Takahashi to the game.

Gameplay:
	Added generic bandit encounters in the Foloi Fields. (They are a little basic at the moment and will be expanded upon at some point in the future.)
	Filled in placeholder content for Yui.
	Added content for the raccoon-girl (Nizhoni) in the centre of Elis's Farmer's Market.
	Added content for the horse-boy (Moreno) in the centre of Elis's Farmer's Market.
	Added new character 'Heather' (human) who runs the fortune telling stall in Elis's Farmer's Market.
	Added new character 'Ms. Levine' (goat-girl) who runs the kissing booth in Elis's Farmer's Market.

Sex:
	During sex scenes in which the sub has less control than the dom, dominant AI sex partners will no longer end sex early (i.e. before the subs are satisfied).
	Loosened requirements a little for the sex actions 'Object to rough' and 'Request rough sex'.

Other:
	Entering the Farmer's Market now places you at one of the four entry points instead of in the centre.
	Clothing types can now be enchanted to have the 'vibration' and 'orgasm prevention' effects if it can be equipped into the groin, vagina, penis, anus, nipple, chest, nipple-piercing, cock-piercing, or vagina-piercing  slots.
	Added a tufted tail type for panther-morphs, which is now assigned to newly-spawned lion-morphs.
	Added ability to perform the 'Quick sex' action in all of Astrai's and Vronti's sex scenes.
	Added ability to resist post-defeat sex with random centauress encounters in the fields (only if noncon is turned on).
	The price of potions and elixirs is now influenced by how many effects they have.

Bugs:
	Fixed visibility of armpit fetishes in the phone's fetish menu being locked behind foot content instead of armpit content.
	Characters without legs can no longer use the 'spread legs' sex action.
	Ralph no longer has randomised personality traits.
	The 'desperate for sex' status effect now correctly only displays during combat.
	Fixed issue where the SLime Queen wasn't correctly spawning wearing her tiara.
	Fixed parsing issues in Lilaya's kimono gift scenes.
	Fixed modding issue where setting an NPC to use a parser tag which had been previously assigned to an NPC wouldn't update the reference, causing the parser tag to always point to the first NPC who was given the parser tag.
	Fixed post-submissive sex with centaur marauder/raider displaying a blank dialogue screen.
	Reformatted potion item effects tooltip to fix an issue where having lots of effects on a potion would overflow the tooltip.
	Pregnant/non-pregnant versions of character artwork are now automatically updated to be used when applicable, instead of requiring a save+load to be shown.
	Fixed issue with several elements in externally-defined sex managers not using their correct default values.

----------------------

PATCH NOTES FOR v0.4.1

Contributors:
	Fixed issues with the parsing engine sometimes forgetting set variables and other parsing targets. (by AceXP)
	Fixed numerous typos and parsing errors in the 'Meraxis's duel', 'Zaranix', 'Wes', and 'Daddy' scenes. (by AceXP)

Engine/Modding:
	The elements 'continuesDialogue', 'travelDisabled', 'inventoryDisabled', and 'regenerationDisabled' in dialogue node modding now all support parsing instead of simply true/false values.
	Added additional 'startingImmobilisation' element to sex manager definitions, allowing you to define characters as starting a sex scene in an immobilised state.
	Externally defined Dialogue Nodes now support parsing for the 'index' element of their responses.

Gameplay:
	Added internal map for 'The Centaur's Sword' tavern in Elis, including the centaur owner 'Kheiron'.
	Added actions to the food and drink stalls in the middle of the Farmer's Market.
	Added 'Fae' and 'Silvia' as two new characters (futa foxtauress sisters) in the Farmer's Market who sell clothing.
	Added 'Kazik' as a character (male ferret-boy) who runs a jewellery stall in the Farmer's Market.
	Added 'Yui' as a new character (female jorogumo) who runs a sex toy stall in the Farmer's Market.
	
Items:
	Added attribute boosts to the following consumables to bring them in line with others: Fizzy Orange Juice; Cotton Candy Soda; Berry Soda; Chamomile Tea; Popcorn; Sausages; Pâté and Crackers; Honey Bread.
	The food items 'Meat and Marrow' and 'Panther's Delight' now give the consumer +1 muscle if their muscles were less than 'muscular' (value of 60).
	Reduced equine cider alcohol content from 15% to 8%.

Sex:
	Added 'armpit slut' and 'armpit lover' fetishes, along with related fetish tease attacks.
	Added in variations for armpit sex for the 'ask for creampie/pullout' and 'encourage creampie/pullout' orgasm actions.
	Added 'bondage bitch' and 'bondage applier' fetishes, which are now associated with the tail, tentacle, webbing, and Witch's Seal restricting sex actions.
	
Other:
	Added 'Dominion', 'Submission', and 'Elis' tabs to the 'map' menu in the phone to make map navigation a little tidier.
	Demon, lilin, elder lilin, and angel essence is now tagged as heavy contraband, so Vicky no longer sells it.

Bugs:
	Parsing fixes.
	Fixed Meraxis always referring to you as her sibling after impregnating her.
	Fixed bug where spinneret depth wasn't being loaded properly, causing it to reload to the default depth every time you loaded a saved game.
	Fixed bug where the game's dialogue would randomly fail to parse in some scenes, resulting in '(Error in conditional parsing!)' messages being displayed.
	NPCs are now only fully deleted after any pregnancies and incubations related to the player have been resolved, which should fix some issues with offspring birth dates and missing information in the pregnancy stats screen.
	Fixed issue where deleted NPCs would cause pregnancy stats, offspring map names, pregnancy tester dialogue, and the debug offspring menu to either throw errors or display as 'Unknown' or '???'.
	Fixed extremely rare bug where it was still possible to impregnate a character who had 0 chance to be impregnated.
	Takahashi now correctly wears a lab coat while in her lab in the citadel.
	Fixed issue where trader responses defined in external dialogue nodes wouldn't work.
	Fixed issue with the 'NPC.applyItemTransactionEffects()' method being called even if the transaction failed to process (such as in the case where the buying character's inventory was full).
	Fixed issue where selecting a disabled action (i.e. a greyed-out button) would still apply whatever effects that action had to the game.
	Externally defined sex managers now correctly handle all missing elements which are tagged as being 'optional'.
	Fixed another issue in externally defined sex managers where the 'slotsAvailable' element's 'slot' elements were not parsing code.
	Externally-defined dialogue nodes will now parse the 'colour' element within 'response' elements, allowing you to use conditional statements and such in them.
	Fixed issue where characters would not get the 'frustrated' status effect after finishing sex without orgasming if they'd orgasmed within the last 24 hours.
	Fixed issue where error log would sometimes display parsing errors when loading a game.
	Added missing quick sex descriptions for tongue-armpits focus.
	Fixed raccoon hair covering being associated with raccoon fur (i.e. the covering for their other body parts).
	Fixed bug with random attackers always spawning as feminine.

----------------------

PATCH NOTES FOR v0.4.0.10

Contributors:
	Replaced depreciated hashmaps with active hashmaps in AbstractClothingType. (PR#1542 by Maxis010)
	Increased script performance by adding a memoization cache to compile scripting engine scripts. (PR#1442 by CognitiveMist)
	Fixed several instances of the 'wall' parser tag not being correctly applied in several sex classes. (by AceXP)
	Fixed parsing errors in TongueVagina sex action class. (by AceXP)

Engine/Modding:
	Added 'applyItemTransactionEffects()' method to NPC.java class which can be overridden to define special behaviour during item/weapon/clothing transactions.
	When defining a 'copyFromDialogueId' element in an external DialogueNode's 'responses' element, the game will now prioritise any responses/tabs you've defined within the 'responses' element, and then fall back on those from the 'copyFromDialogueId' element (i.e. you can now override responses/tabs from the copied dialogue node).
	Added a 'wallName' element to xml sex managers so that you can set the name of walls in sex scenes.
	Moved all kimono clothing into external res files.

Gameplay:
	Added a small side quest for unlocking the spells from the arcane lightning globe (which is found in the warehouse during Claire's teleportation quest). If you have the globe in your inventory, you'll be able to ask Arthur about it to start this quest.
	Filled in all of Meraxis's placeholder content, and added the option to have sex in her room after you've unlocked vaginal, oral, and anal (if anal content is enabled) actions with her.
	Added an internal map for the Farmer's Market in Elis. (It's all placeholders at the moment, but will be filled in for the next update.)
	Added demonic centaur encounters which can be triggered in the Foloi fields, Hubur river, and grassland wilderness tiles in the world map. (These encounters are quite basic and will be expanded upon in future updates.)

Items:
	Added 'battle axe' weapon (two-handed, all damage types, sold by Vicky).
	The 'dory' spear is now sold by Vicky.
	Added 'short kimono' as a short-skirt variation of the kimono. Also made the flowers on the kimono into a 'sticker', which can be removed so as to make a plain kimono. Also added a new 'blossom' pattern for the kimono.

Sex:
	Tagged 'tentacle-squeeze' and 'tail-squeeze' as being sadistic actions, and added non-sadistic actions 'tentacle-massage' and 'tail-massage' as an alternative for non-sadistic characters. (These 'massage' actions are available to sadistic characters in addition to the 'squeeze' actions.)
	Enabled availability of forcing creampies and asking for pull-out or creampie for when a character's spinneret was the orifice being penetrated by their partner's cock.
	Added sex actions to cast and dispel the immobilising effects of the spell 'Witch's Seal' on your sexual partners, so long as you know the spell (obtained from equipping a Witch's broom) and have full control in the sex scene.

Other:
	Added 'spinneret creampie' status effect, so cum now correctly leaks out of a creampied spinneret over time.
	Added correct tracking of spinneret virginity loss, and added spinneret penetration/virginity loss descriptions to sex.
	Added 'Automatic text copying' as a new option (disabled by default). When enabled, the current scene's text will automatically be copied to your system's clipboard every time a new scene is loaded. This option is so that you can easily paste the game's text into text readers without needing to select and copy the scene's text every time.
	NPCs will now have more variance in the following body parts: ass and hip sizes, femininity, muscle, body size, nipple and areolae size, crotch nipple and areolae size, and lip size.
	Quests are now ordered in the phone menu based on whether they're completed or not.
	Added additional menu 'Misc. spells' in the spell menu to see what spells are available from weapons/unique events.
	Renamed the race & subspecies of 'cow-morph' to 'cattle-morph', and changed the male name from 'cow-boy' to 'bull-boy'.
	Greatly increased lust resistance for characters with low levels of corruption: 'pure' level 5->25; 'vanilla' level 0->15; 'dirty' 0->5.
	Lyssieth's sex scenes are no longer locked to the 'over desk' position, and instead start in the 'standing' position, from which normal positioning options are now available.
	Added variation to the demon TF scene with Lyssieth so that you can prevent her from growing a cock.
	The Foloi Fields and Hubur river tiles in the world map are now classified as dangerous, due to the new demonic centaur encounters being in these areas.
	Added 'Explore' action to the Foloi fields, river Hubur, and the grassland wilderness, which just provides a more convenient method of trying to trigger a random encounter instead of having to travel back and forth.

Bugs:
	Typos and parsing bugs fixed.
	Fixed bug where the count of total unique sex partners would always start at 1. 
	Fixed issue where Vengar would get stuck on the Milking Room tile after losing the fight to him.
	Fixed bugs where loitering or sleeping for multiple hours at a time could cause multiple generic NPCs to spawn and get stuck in Angel's Kiss and on Dominion alleyway tiles occupied by a prostitute.
	Bat-morphs in the bat caverns will no longer spawn without having bat-morph arms.
	Fixed issue where Meraxis would sometimes not move to the tile she was supposed to be in.
	Fixed the spell 'Witch's Seal' being classed as an air school spell instead of arcane.
	Sadist fetish text now correctly indicates that it unlocks sex actions.
	Fixed issue where Lyssieth would not return to her human form after having lilin-form sex.
	Fixed issue where the post-Lyssieth sex scene in Meraxis's office indicated that Meraxis was present, even if she had relocated to Elis.
	Elis internal maps now correctly have 'against wall' sex position available in them.
	Added ability to stop Rose's hand-holding sex scene to prevent you from getting stuck in it if you weren't able to orgasm.
	The 'Grow cock' sex actions now correctly give larger penises to leg configurations which have large genitals.
	Fixed bug where the 'companionsAreAllies' element in a response's 'combatVariables' element would not work correctly and throw background errors when set to true.
	NPCs who have sexual histories with the player are now fully deleted when removed from the game, instead of simply being moved to the generic holding tile. This will retroactively apply when loading into this version, and should help to cut down on save file size and end turn lag.
	Fixed bug in sex managers defined in external files where repeat instances of using the sex manager with non-unique NPCs would throw background errors.
	Fixed issue where the 'incubated offspring' list in the pregnancy stats screen was showing all non-incubated offspring instead of incubated offspring.

----------------------

PATCH NOTES FOR v0.4.0.8

Contributors:
	Fixed a bug where dialogue flags would not be loaded correctly if your save had broken mods in it, resulting in many potentially game-breaking effects. (by AceXP) Innoxia's note: If your game has experienced bugs related to the resetting of knowledge about quests, the calendar, essences, etc., then I would advise you to load an older save before that happened or start a new game (sorry for the inconvenience). 
	Added functionality to debug menu to show the chances of encountering various races in the current location - added in the 'Misc.' tab, 2nd page as 'Spawn rates' action. (PR#1531 by AceXP)
	Added a special attack, 'talon slash', to characters that have taloned feet (i.e. harpies). The base damage is 20 (same as a kerambit). If the attack does damage, extra damage is applied as a critical effect. (PR#1530 by AceXP)
	Made some optimisations to the GameCharacter.getChildren() and GameCharacter.getNonCommonNodes() methods to decrease save times by around 33%. This change is most noticeable on games with a large number of offspring. (PR#1533 by Sarkath)
	Fixed issue where the key for locked clothing that was unequipped during sex was being removed from the unequipper's keys, even though the item was automatically re-equipped after sex resulting in the unequipper not having the key. (PR#1541 by debouchere)
	Fixed a huge amount of typos and consistency errors in dialogue. Full patch notes for this PR are at the bottom of these patch notes. (PR#1550 by AceXP)
	Fixed a NullReferenceException which was being thrown whenever a slave laying incubated eggs hadn't previously birthed live young. (PR#1551 by Maxis010)
	Fixed some parser bugs and improved HLFQuest UX by adding button to search for password and improving firebomb quest descriptions and triggers. (PR#1547 by DSG)
	Refactored all of the existing 'Self' type sex actions from 'Player/Partner' into shared actions. (PR#1539 by Maxis010)
	Added more detailed rabbit-morph lore. (by Manwhore)
	
Sex:
	Sadistic sex actions are now only available to characters who have the 'sadist' fetish.
	Set 'slap ass' as a sadistic action, and added 'spank ass' as an alternative that's available to characters who don't have the sadist fetish.
	Added tongue-armpit sex actions (i.e. licking armpits), which are available in any position that allows tongue-breast interactions. (Armpit content can be disabled in the content options.)
	
Other:
	Renamed the actions for entering Elis to 'Enter (main)' and 'Enter (rear)'.
	The 'aristocrat' occupation is now recognised by Leotie as being a suitable occupation at the start of her test.
	Added 'eggs implanted' and 'eggs incubated' as tattoo counter types.

Bugs:
	Typo and parsing fixes.
	Fixed issue where Loppy's artwork wasn't being displayed.
	Fixed bug where over 24 hours would sometimes pass when using Astrapi's centaur ride for the first time, and also fixed a related bug where Vronti's journeys would always pass over 24 hours.
	Fixed issue where tattoo cum counts would not increment for slaves who were having sex with generic characters. (e.g. When they were having sex in the brothel or in the stocks or with other slaves.)
	The 'Forced chastity (desperate)' status effect will no longer be reset to 'Forced chastity (calm)' after every save/load.

AceXP's PR#1550 Patch Notes:
	Typos:
		Dragon leg transformation mentions fur, should be scales.
		Mommy's nice and full and today -> Mommy's nice and full today.
		Remove extra ) at the end of dialogue with pregnant npc.
		out of this area ... -> out of this area...
		candi pouts -> Candi pouts.
		greedily kissing and kicking the cougar-girl -> greedily kissing and licking the cougar-girl.
		take out the shotgun -> take out the rifle (DSG HLF bolt rifle)
		centuar -> centaur
	Consistency:
		River Huber -> River Hubur.
		One Night in June -> One Day in June.
		Bat cavern attacker mentions two-hundred and fifty flames, should be five hundred flames.
		Red light district -> Red-light district.
		Nyan: I'm on the second floor -> I'm on the third floor.
		Opening hours of the Watering Hole should display in 12/24 hour clock format
	Bugs:
		Parser error with kilometers/miles when the world map is mentioned.
		Parser error in the stocks if you have a companion.
		appears to be in his past seventy -> appears to be past seventy
		Several text fixes and other issues in Helena's quest and Dominion Express content
		Fixed switched text for single/multiple tails while petting
		Thoughts should not be muted (also change dialogue for alleyway demon attacker)
		Minor octopus morphs spawned with eight HUMAN legs.
		Changed some occurences of step and walk to user parser commands [pc.step] etc.
		After freeing a slave a Freedom certificate should be removed from the inventory.
		Clothing that is discarded on use (condom, web seals) should be removed from the game when doing Unequip all.
		Fixed info text for changing pubic hair mentioning no genitalia when that is not true.
		Fixed (not solo) handjob climax looking weird when the character is giving themselves a handjob.
		Fixed elemental birth date of 29 february leading to Exception
		Fixed self-TF menu leading to NPE with <ableToSelfTransform>true</ableToSelfTransform> race
		Fix issues with Bunny/Loppy pregnancy (also move Loppy images to KT80 folder)
	New features:
		Added missing penetration length code for tentacles.
		Add the rolled-up posters to the encyclopedia when you get them, as you can never see them otherwise.
		Add crawl/slide as movement verbs for cephalopods.

----------------------

PATCH NOTES FOR v0.4.0.6

Contributors:
	Deprecated the toc.xml in favour of file name based sorting for patch notes. (PR#1537 by Stadler76)

Bugs:
	Typo fixes.
	Fixed issue where NPCs would not be present in their intended home cells when creating a new game, which was affecting all unique NPCS, most noticeably harpies and shop keepers in the Shopping Arcade. If you made a new game in 0.4.0.5, I'd advise starting over as I haven't retroactively fixed these NPCs being in incorrect tiles (as it would take a long time to go through them all and check where they're meant to be). 
	The underarm content toggle should now correctly disable the availability of armpit actions in sex.
	Fixed issue where exiting Dominion into the world map would sometimes place you in the last world map location you'd been in instead of the Dominion tile.
	Removed the 'Masturbate' action when accepting Meraxis's duel (which I was using for debugging purposes but forgot to remove it for the release).
	Fixed issue with Meraxis's post-kiss actions' tooltips incorrectly stating that sex areas were inaccessible.
	Fixed a couple of bugs related to the issue where trying to use the centaur transport back to Dominion from Elis would not work correctly.
	Fixed issue where you had to use the 'Wait' action twice at the Elis centaur depot for Astrapi or Vronti to appear.
	Fixed another centaur depot issue where the 'Introduction' scene would replay when using the 'Wait & enter' action at the Dominion depot.
	Fixed issue where Astrapi or Vronti would get stuck on the depot tile at ELis when choosing the decline their offer of a ride.
	Fixed (the final) issue with centaur transports where the time would not progress properly on your route to/from Dominion when travelling during the hour of 06:00.
	Fixed issue where the game would sometimes become unresponsive when more than one generic NPC spawned on the same tile (which happened most often when Enforcers were spawned).
	Fixed some slight awkwardness in the flow of dialogue when looking at the calendar in your room.
	
----------------------

PATCH NOTES FOR v0.4.0.5

Contributors:
	Updated lilithsThroneBuildTutorial.md. (by AceXP)
	Fixed bug where Angel's Tears didn't reset the consumer's lust value like it should. (by AceXP)
	Fixed bug where imp gangs would have elixirs with no effects in their inventories if the player was a slime. (by AceXP)
	Fixed minor issue with random generation not being as random as it should have been. (by AceXP)

Engine/Modding:
	Added support for world and place types to define whether walls are present (which enables the 'against wall' sex position).
	Added support for sex actions to be applied at the start of sex when using the sexVariables element in responses.
	Added framework for external sex manager support, granting significantly more control over how sex scenes play out. (You can see a commented example in 'res/sex/innoxia/managers/meraxis/masturbation.xml')
	When defining dialogue nodes, added the ability to copy responses from another dialogue node instead of having to copy+paste them. (Done by using 'copyFromDialogueId' attribute in the 'responses' element.)
	Improved the 'random' parsing command so that empty strings are discarded from the potential returns, allowing you to use conditional statements to allow or remove strings from the randomly selected pool.
	Added new CoverableArea value 'ARMPITS', and applied this value to all applicable blocked body parts for 'torso over' and 'torso under' clothing in the game.

Gameplay:
	Re-enabled ability to leave Dominion. (Note that demonic centaur encounters aren't yet enabled in the fields, so there's not much to do there yet.)
	Enabled entry to Elis. (Note that while all the places in Elis have dialogue, there isn't much to do there yet outside of the content in The Red Dragon.)
	Added Meraxis dialogue for when leaving Dominion for the first time.
	Added Meraxis dialogue in The Red Dragon.
	Added two new unique centaur characters ('Astrapi' and 'Vronti') who together provide transport between Elis and Dominion (includes sex scenes for both characters).
	Added interactions with Flash in The Red Dragon (talking and buying drink/food).
	Added interactions with Jess in The Red Dragon tavern (paying for her company and sex), and added voyeurism scene at her bedroom when she's entertaining a client.

Items:
	Added weapon 'arcane recurve bow' (two-handed, ranged, physical/ice/fire/poison damage, sold by Vicky).

Sex:
	Added armpits as a new sexual 'orifice'.
	Added penis-armpit sex actions, which are typically available in the same positions that penis-breast actions are available.

Other:
	Added new content toggle for armpit content. (On by default.)
	Roughly halved travel time for all fields tiles in the world map.
	Reduced the values of several drink items.

Bugs:
	Parsing and typo fixes.
	Fixed badger foot type being hoofs instead of paws.
	Fixed 'barren' and 'firing blanks' perks being detected as physical perks instead of sex ones.
	Added missing description for mouth-foot sex actions in quick sex overview screen.
	Fixed issue with incorrectly parsed descriptions for when orgasming during an ongoing self-cock stroking action.
	Added handling for several errors when loading saved games from several versions ago.
	The 'anus' status effect during sex will no longer be displayed if anal content is turned off in your content options.
	Fixed the export character screen saying that the export button was in the top-right instead of bottom-right.
	Fixed tongue-nipple dirty talk referencing penetrating the nipple even if the target's nipples were not penetrable orifices.
	Fixed issue where banned sex areas would sometimes become available after changing positions in special sex scenes.

----------------------

PATCH NOTES FOR v0.4

DSG's HLF Quest (PR#1398):
	Added a new side quest which adds some details of the background lore of the Human Liberation Front (HLF), which was previously explored in Wes's quest.
	Quest can be triggered when exploring the dark tiles in the Bat Caverns.
	Added 8 new items of clothing (all of which can be obtained during this quest, and all of which are unisex), and 2 new clothing sets ('HLF Regular' and 'HLF Insurgent'):
		Skull-patterned bandana (mouth slot).
		Boonie hat (head slot).
		Canvas webbing (over-torso slot, HLF Regular set).
		Vintage fatigue trousers (leg slot, HLF Regular set).
		Vintage fatigue tunic (torso slot, HLF Regular set).
		Vintage combat boots (foot slot, HLF Regular set).
		Canvas brassard (wrist slot, HLF Insurgent set).
		Canvas bandolier (over-torso slot, HLF Insurgent set).
	Added 5 new weapons (again, all of which can be obtained during this quest):
		Arcane firebomb (fire damage, ranged, 2-handed, destroyed after 1 use) - these have an additional associated side quest, the completion of which allows you to get more made. (Innoxia: 'I'll make them 1-handed once I've added throwable weapon framework.')
		Pepperball submachine gun (fire damage, ranged, 2-handed, requires 2 essences to fire, grants 'Spray 'n Pray' special attack).
		Pepperball revolver (fire damage, ranged, 2-handed, requires 1 essence to fire, grants 'Fan the Hammer' special attack).
		Teargas shotgun (poison damage, ranged, 2-handed, requires 4 essences to fire).
		Pepperball bolt-action rifle (fire damage, ranged, 2-handed, requires 3 essences to fire).

Jam's artwork (https://twitter.com/JamDrawers):
	Added 3 images for Helena.
	Added 4 images for Angel.
	Added 4 images for Epona.
	
KT80's artwork (https://twitter.com/KT80AT):
	Added 2 images for Claire.
	Added 3 images for Bunny.
	Added 3 images for Loppy.

Contributors:
	Fixed issue where Enforcer patrols wouldn't spawn correctly. (by AceXP)
	Fixed bug where non-human coverings wouldn't appear as recolouring options in Helena's slave creator. (by AceXP)
	Fixed minor parsing issue with Enforcer Patrol description during arcane storms. (by AceXP)
	Fixed issue where a background error would something be thrown in sex, softlocking the scene. This was being encountered most frequently in Frysia's sex scene. (by AceXP)
	Fixed bug where arachnid leg descriptions had a parsing error in them. (by Stadler76)
	Added feature where if an offspring's father and/or mother has generic wings (feathered, leathery or insect) or horns (curled, curved, straight, etc.), the offspring can inherit them. (PR#1370 by Stadler76)
	Suppressed descriptions of nipples as orifices and transformation options for nipple penetration when that content was turned off in user settings. (PR#1421 by AceXP)
	Added 'Elasticity depth effects' mechanic: If an orifice's elasticity is at least 'limber', its maximum uncomfortable depth is increased, with greater elasticity values increasing it further. This is off by default, but can be turned on in content settings. (PR#1413 by LightCanadian)
	Modified UtilText.java to properly handle a few inaccurate British to American translations. (PR#1447 by TadUnlikely)
	Added offspring inheritance of ferality. Feral mothers now always birth feral offspring. Offspring which take after the father born to a non-feral mother and feral father will always be fully furry. (PR#1451 by Stadler76, modified by Innoxia)
	Prevented strap-ons from being equipped when there is one already equipped (in another slot). Also fixed issue where covering colour for an equipped dildo was potentially being incorrectly referenced. (PR#1453 by AceXP)
	Reduced the minimum wing size for allowing flight for feral quadrupeds to 'THREE_LARGE'. (PR#1454 by Stadler76)
	The 'Cum Stud' fetish now gives the same affection bonus from the milking slave job as the 'Lactating' fetish. (PR#1460 by Eliria)
	Added a new 'Winged biped' LegConfiguration for use for feral bats and wyverns. (PR#1486 by Stadler76)
	Made Enforcer disguises more difficult to pull off and added flavour text for when impersonating (or failing to impersonate) specific Enforcers. (PR#1501 by DSG) 
	Fixed bug where if the game was installed in any folder with 'res' in the name, then viewing book entries for external/modded races in the encyclopedia would throw errors. (by Stadler & AceXP)
	Fixed issue where place tiles were not being populated with regional subspecies in the world map. (by AceXP)
	Fixed some issues with hard-coded values for NPC spawning in the Bat Caverns, allowing spiders to spawn down there too. (PR#1514 by Stadler)
	Fixed issue with spider-morphs sometimes incorrectly spawning as the tarantula subspecies. (included in PR#1514 by Stadler, fix by Charisma)
	Added correct self-transformation options for youko (and any other applicable races with self-TF powers). Added special youko tail perks to track youko tail counts. Also enabled changing secondary coverings colours for Elementals, and changed ice description to glittering instead of shimmering. (PR#1506 by AceXP)
	Refactored code to automatically generate essences for all races. (PR#1507 by AceXP)
	Relocated patch notes to HTML files. (PR#1511 by Stadler76)
	Fix numerous parser errors and typo fixes, mostly with external race files. (PR#1515 by AceXP)
	Added 'UNENCHANTABLE' as a new item tag, which greys out an item's enchant button in the inventory as if it were a normally unenchantable item type. (PR#1517 by cimds)
	Fixed bug where 'handjob climax' sex action was describing the orgasming character cumming into their own hands, but their partner's hands were the ones that ended up dirty. Also added handjob climax action to masturbation scenes. Fixed some parser errors with Bunny and Loppy at Angel's brothel. Added wash action after seeing a client at Angel's brothel. (PR#1528 by AceXP)
	Fixed issue with loading NPCs introduced in 0.4. (PR#1529 by AlacoGit)
	Tidied up some code and simplified some methods for easier race modding. (PR#1523 by Stadler76)
	Hyena lore book typo fixes, adjusted spotted hyena heights to fit in with lore. (by Manwhore)
	Fixed issue where starting a new game would sometimes throw background errors. (by Stadler76)
	Added some flavour text at Lilith's Tower, Enforcer HQ, and the statue in Slaver Alley for if the player has the tourist occupation. (by DSG)
	
DSG's clothing contributions:
	Added 'women's leather jacket' (over-torso slot, feminine, sold by Nyan). (by DSG) (The women's leather jacket already in the game has been renamed to 'Women's fashionable leather jacket'.)
	Added 'vintage field jacket' (over-torso slot, masculine, sold by Nyan). (by DSG)

C4MG1RL's 'Benevolent Blessing' clothing & weapon set contribution:
	Added status effect and set bonus for 'Benevolent Blessing'. These three clothing items are all unisex and part of this Benevolent Blessing set. These items will be used along with the trickster set during the youko content later on, so can only be spawned via the debug menu for now.
	Added 'kyudogi' (torso slot).
	Added 'mitsugake' (hand slot).
	Added 'benevolent necklace' (neck/wrists slot).
	Added weapon 'Hama Yumi' (ranged, two-handed, ice/fire/poison damage types).
	
Sage's 'Latex Lover' clothing set contribution:
	Added status effect and set bonus for 'Latex Lover'. All of the following are sold by Finch.
	Added 'latex crop top' (torso slot, unisex)
	Added 'latex zip bra' (chest slot, feminine) 
	Added 'latex corset' (stomach slot, feminine)
	Added 'latex panties' (groin slot, feminine)
	Added 'latex elbow-length gloves' (hands slot, unisex) 
	Added 'latex arm warmers' (hands/wrists slot, unisex)
	Added 'latex thigh-high stockings' (calves slot, unisex)
	Added 'latex open thigh-high stockings' (calves slot, unisex)
	Added 'latex bodysuit' (stomach slot, feminine)
	
Engine/Modding:
	Added BodyPartTag 'HAIR_IGNORE_PLAYER_SETTINGS', which tags hair types as always being present on furry heads, even if the player has 'furry hair' turned off. This is applied to hyenas.
	Added 'genericType' fields for Wing and Horn xml files, so that you can define those types as being generic (not associated with any parent race) or not.
	Fixed spelling error of 'DISBALE_' instead of 'DISABLE_' in SubspeciesFlag values (I added a catch for this in the code so even if your mod has the incorrect spelling it won't break).
	Added 'flags' as a parser target for quicker access to 'game.getDialogueFlags()'.
	Added 'CORRUPTION_LEVEL_' prefix as a parsing hook to the CorruptionLevel enum.
	Added a few methods to the game class  to give you hooks to some useful UtilText methods: parseFromFile(); addSpecialParsingString(); and clearSpecialParsingStrings().
	Added support for defining maps (both WorldType and PlaceType classes) as external xml files, which will (soon - hopefully in 0.4.1) allow for map modding.
	Added support for defining DialogueNodes and Encounters as external xml files, which, like the maps, will (soon - hopefully in 0.4.1) allow for scene modding.

Gameplay:
	Updated descriptions of fields, river, woods, grassland, and Dominion tiles in the world map.
	Added maps for Elis, Elis's shopping precinct, The Red Dragon tavern (both floors), and Elis town hall (both floors).
	Added several new unique NPCs for Elis content.
	The arcane storm status effect message will no longer interrupt scenes if the player character is not within Dominion itself.
	Added badger race, along with 'Black Stripes Perry' and 'Berry Trifle' as the related drink and food consumables. (Thanks to DSG for creating the trifle image!)

Weapons:
	Added 'dory' spear (melee, one-handed). (Thanks to DSG for svg edits.)

Sex:
	Added 'tentacle-squeeze' and 'tail-squeeze' as miscellaneous sex actions which can be performed once a character is restricting their partner via their tentacles or serpent-tail. (These sex actions have sadist/masochist fetishes associated with them.)

Other:
	Zaranix is now still called 'Zaranix' when in his feminine form, instead of 'Zoelix' (as the name change wasn't being mentioned anywhere or referenced at all, and didn't make much sense).
	Tidied up Zaranix's post-combat dialogue and added variations for if non-con is turned off, as well as for the player to request Zaranix to transform into succubus form after swallowing his TF potion.
	Made it so that Zaranix's oral sex scenes now start with you already sucking his cock, instead of having to wait for him to deal with clothing displacements first.
	The 'flared' and 'tapered' penetration modifiers are now mutually exclusive with one another.
	Added 'Set spawns' action in debug menu, so that you can easily spawn in all items of any clothing set.
	Added 'light brown' as a covering colour.
	Added elder lilin damage attribute so as to separate lilin and elder lilin damage perks.
	Added functionality to sort saved games by date or alphabetically.
	Changed 'men's hakama' from being masculine to unisex, and changed the name to just 'hakama'.
	Added light green as a covering colour.

Bugs:
	Minor typo and parsing fixes.
	Fixed actions to play dice poker at tables in the gambling den not being greyed out if you didn't have enough money to play.
	Pate and crackers will now correctly restore 20% health/aura instead of 5%.
	Fixed issue where Zaranix (and maids) would sometimes not revert to their default bodies after you'd left his home.
	You will now exit onto the correct tile when leaving Zaranix's home post-combat, instead of exiting onto a random demon home tile.
	Fixed bug where you could escape from combat with Zaranix.
	After resolving Zaranix's quest peacefully, Amber will no longer be so angry on your first repeat visit.
	Fixed bug where you couldn't go upstairs in Zaranix's house before going to encounter Katherine.
	The starting action for Arthur's hypno-watch quest is now correctly coloured as a side quest.
	Fixed oral foot worship sex types having no descriptions in quick sex scenes.
	Fixed bug where maximum penis girth TF from clothing was capped at value 6 instead of 7.
	Fixed issue where the kitty clothing set bonus wasn't being applied.
	
----------------------

PATCH NOTES FOR v0.3.20

Contributions:
	Fixed issue where some subspecies would spawn in canal tiles, even when their spawn rate is supposed to be zero. (by AceXP)
	Fixed bug where Natalya would be a regular succubus in new games, and not a demonic centaur - the fix will apply when loading into this version for if she's affected by this in your game. (by AceXP)
	Prevented Enforcers from inadvertently spawning as slimes. (by AceXP)
	Updated dragon lore entries. (by DSG)
	Fixed parsing error in spinneret webbing special attack. (by Stadler76)

C4M's clothing contributions:
	(Note that these can only be spawned via the debug menu for the time being.)
	Added 'Trickster's Mask' (eyes slot, unisex).
	Added 'Trickster's Cloak' (over-torso & neck slots, unisex).
	Added 'Trickster's Tunic' (torso slot, feminine).
	Added 'Muramasa' weapon (melee, lust damage, one-handed).
	Added 'trickster' clothing set bonus for the above items.
	
TonyJC (creator) & NeverLucky (editor) clothing contributions:
	Added 'cropped tank-top' (feminine, torso slot, sold by Nyan).
	Added 'cropped sweater' (feminine, over-torso slot, sold by Nyan).
	Added 'cropped T-shirt' (androgynous, torso slot, sold by Nyan).
	Added 'daisy dukes' (androgynous, leg slot, sold by Nyan).
	Added 'denim overalls' (androgynous, leg slot, sold by Nyan).
	Added 'one-strap crop top' (feminine, torso slot, sold by Nyan).
	Added 'shoulderless sweater' (feminine, over-torso slot, sold by Nyan).
	Added 'sleeveless shirt' (androgynous, torso slot, sold by Nyan).
	Added 'spaghetti crop tank-top' (feminine, torso slot, sold by Nyan).
	Added 'tank-top' (androgynous, torso slot, sold by Nyan).
	Added 'tied-up croptop' (feminine, torso slot, sold by Nyan).

Engine/Modding:
	Added 'spreadsHerLegs' parsing command for handling the possibility of characters with no legs when describing 'spreads her legs'.
	Added ability to set 'additionalFootStructure' elements in modded 'leg' xml files, so you can set which foot structure is used by default for that leg type based on different leg configurations.
	Added 'TAIL_ATTACK' BodyPartTag for setting whether a tail is suitable for being used for the 'tail swipe' attack.
	Added 'HARPY_NESTS' as a world region, which prevents all Dominion races from showing up in the 'characters present' tooltip in the Harpy Nests.
	Defining a horn length of '0' in RacialBody.xml files will now force that femininity to spawn with no horns (updated hyena's RacialBody.xml file with comments on how this works).
	Added an optional 'nameTransformation' field to coveringType files so that you can set a name for the covering to be used in transformation menus (see 'race/innoxia/sheep/coveringTypes/wool_face.xml' for an example).

Races:
	Added orange skin colour.
	Changed covering type of harpy legs from being feathers to bird skin.
	Added 'swan-harpy' as a subspecies of harpy, requiring white feathers and either grey or ebony leg skin to be identified as one. Helena is now a swan-harpy.
	Added 'sheep-morph' race.
	Added 'Ewe's Brew' (dandelion tea) consumable drink for the sheep-morph's attribute item.
	Added 'Wooly Goodness' (candy floss) consumable food for the sheep-morph transformative item.
	Added 'goat-morph' race.
	Added 'Pan's Flute' (champagne) consumable drink for the goat-morph's attribute item.
	Added 'Billy's Best' (goat cheese) consumable food for the goat-morph transformative item.
	Added 'pig-morph' race.
	Added 'Porcine Pop' (cola) consumable drink for the pig-morph's attribute item.
	Added 'Oinkers Fries' (curly fries) consumable food for the pig-morph transformative item.

Other:
	You can now additionally apply the vibration enchantment to clothing which fits into the nipple, chest, penis, vagina, nipple-piercing, vagina-piercing, or cock-piercing slots.
	Added a few more items of clothing to the choices in character creation.
	You now require a bipedal leg configuration to be transformed into a demon.
	Added ability to set spider eyes as heterochromatic.
	Updated Angel's clothing.
	NPCs with a cloaca will no longer spawn with an equipped buttplug or chastity cage.
	Greater spider-morphs now have a 50% chance to spawn with 6 arms.
	Prevented rabbit and harpy tails from ever being suitable for penetration.
	The 'tail swipe' attack is now only available to alligators, sharks, and dragons who have a tail length greater than 1 metre.
	Safety goggles no longer spawn on the floor in Lilaya's lab (although they won't be removed if they're already spawned in your game). Instead, you can ask her for a spare lab coat (which gives you safety goggles as well).
	Cow-eyes now correctly have horizontal pupils by default.
	Made the 'furry hair' content option disabled by default (this won't affect your current settings).
	Wolf-morphs and border-collie-morphs now have +25% sheep-morph damage as part of their subspecies status effect.
	Added body size increase as an effect of the brown rat's burger.

Bugs:
	Parsing fixes.
	Fixed issue in sex scenes where background errors would be thrown and potentially softlock the game when an anal fetishist orgasmed while receiving anal and having an empty vagina.
	Fixed issue where Helena's old slaves could get stuck on her shop tile and never despawn.
	Fixed bug where trying to open your inventory during character creation would throw background errors.
	Fixed issue where Dominion muggers were not using outfit files and so were spawning with completely random clothing.
	Added catch to handle error if actions for partners in sex were not being generated properly.
	Removed all references to 'legs' for characters who don't have legs (i.e. if they have a snake's tail instead of legs). If you find any references to your 'legs' while playing as a lamia or other similar race, please let me know.
	Fixed references to your character laying multiple eggs in Lilaya's birthing scenes if you only had one egg to lay.
	Fixed issue with arachnid leg configurations describing their feet as plantigrade.
	Characters being bred in the pregnancy roulette game can no longer stroke their own cock.
	Fixed issue with the 'unlikely whammer' burger spawning when silly mode was turned off.
	Fixed incorrect tooltip for the friendly occupant petting action.
	Fixed issue where the Enforcer bowler hat commissioner badge was using the same icon as the commissioner oak leaves.
	Fixed issue with taur sapwn rate not working as intended.
	Fixed bug where all taurs would spawn with horns, even if their race shouldn't have horns by default.
	The 'cocoon'/'constrict'/'tentacle restraint' sex actions now correctly become greyed-out when unavailable.
	Spinnerets are no longer incorrectly blocked by clothing which conceals a character's ass.
	Fixed issue where some items of clothing would spawn with incorrect colours (such as the feminine and masculine watches).
	Fixed bug where spider-morphs were sometimes spawning as tarantula-morphs.
	Fixed bug where Rose would have her home tile set to Lilaya's lab instead of her room.
	Fixed Youko race status effect displaying '0 corruption'.
	Fixed bug where you could encounter half-demons of non-Dominion races on canal tiles.
	Fixed bug where unarmed damage attribute was being applied as a damage modifier three times, making unarmed attacks far more powerful than intended.
	Fixed issue in combat where if your AP fell to 0, you could never win or lose combat due to being permanently stunned.
	Fixed some issues with importing characters which were exported in earlier versions.

----------------------

PATCH NOTES FOR v0.3.19

Contributions:
	Fixed issue where spider-morph book's front cover icon wasn't visible. (by NeverLucky)
	Added furred spider tail as a TF option for spider TF potions. (PR#1510 by Stadler76)

Engine/Modding:
	Added parser hook for BodyCoveringCategory using the prefix 'BODY_COVERING_CATEGORY_'.
	Added BodyPartTag 'TAIL_TAPERING_BULBOUS' for defining the shape of spider abdomen-like tails.

Other:
	Added 'hug' and 'pettings' actions to interactions with characters staying in the mansion as your guest.
	Changed name of spider TF item from 'Chocolate Coated Cocoa Beans' to 'Chocolate Coated Coffee Beans'.
	Added ability to regrow or remove hymen via the self-TF menu.
	Added dirty talk variations for tribbing.

Bugs:
	Typos, grammar, and parsing fixes.
	Fixed bug where trying to set a slave free would throw background errors and cause buttons to become unresponsive.
	Fixed bug where Helena would sometimes end up trying to sell more slaves than she actually owned.
	Fixed related issue where Helena's slaves would not be correctly initialised if you were standing on her shop tile at the moment new slaves were generated.
	The 'Dispel elemental' action now works correctly for companions.
	Fixed bug where you'd sometimes lose a proportion of your health and aura when loading a saved game.
	Fixed bug with the new 'Aristocrat' background, where your corruption would double every time you loaded your game. Also fixed related issue where the derived resistances from aristocrat's corruption would be incorrectly saved and loaded.
	Fixed rare cases where nested else/if statements would parse incorrectly.
	Fixed issue with some non-bat tails being referred to as 'bat' tails.
	When freeing Scarlett (and therefore triggering her body to be reset to her harpy form), she now correctly returns to having her default fetishes, and also no longer regains her anal virginity if she'd lost it while being your slave.
	Fixed issue where spider-morphs with an arachnid leg configuration wouldn't have a spinneret.
	Spider-morphs will no longer spawn with crotch-boobs by default.
	Fixed bug where a spinneret's orifice covering wouldn't be coloured according to the character's skin colour.
	Fixed error log entries related to item spawns being generated when spawning a spider-morph attacker.
	Fixed the save/load menu having very dark row background colours when in light mode, which was making it impossible to read saved game names.
	Fixed issue where all clothing stickers would be unlocked by turning debug mode on, instead of the actual sticker unlocks mode.

----------------------

PATCH NOTES FOR v0.3.18

Charisma's spider-morph contribution:
	Added spider-morph race.
	Added spider-morph and tarantula-morph subspecies.
	Added 'Jet Black Coffee' and 'Chocolate Coated Cocoa Beans' for the spider-related attribute and TF items.

DSG's race's updates (PR#1500):
	Non-mythical race bonuses were adjusted so taht the total more closely matches the magnitude of the game's other non-mythical races.
	Total of race bonus values for mythical races (dragons, gryphons) were aligned to the same range as demons and alicorns (demons/dragons at 180, alicorns at 165, gryphons at 150).
	Fixed a tertiary color issue with dragon overlays, tweaked shark finned ear description.

Contributors:
	Added option for the bandana to be worn in the neck slot. (by DSG)
	Fixed huge issue with performance, making turn times roughly 30-50% faster. (by AceXP)
	Fixed incorrect inventory contents of attackers spawned via the debug menu. (by AceXP)
	Fixed issue with clit size not being able to be changed in character creation. (by AceXP)
	Fixed issue with modified fluid colours being saved. (by AceXP)
	Fixed issue with Gryphons (and other low spawn rate subspecies) not spawning as Enforcers. (by Stadler76)
	Fixed issue where 'Warning: getClosestStringMatch()' entries would be shown when there was just a difference in capitalisation. (by AceXP)
	Slimes and bats in the bat caverns will now correctly spawn with weapons. (by AceXP)
	Added expanded hyena-morph lore in the 'Laughing Hyenas' lore book. (by Manwhore)
	Added unique icon for border-collie morphs and gave bald-eagle harpy icon a coloured beak. (by NeverLucky)
	In subspecies XMLs, if secondaryColour or tertiaryColour elements are empty they now default to colour. (PR#1503 by Stadler76)
	Added several new methods in Body.java and BodyPartTypeInterface.java and used these methods to tidy up xml race files. (PR#1498 by Stadler76)
	Fixed issue where becoming a demon didn't work for several LegConfigurations since the setLegsToDemon() method for those LegConfigurations wasn't implemented. (PR#1496 by Stadler76)
	Fixed the body tooltip information for antenna to reflect changes to the number of antenna per row. (PR#1494 by debouchere)
	Fixed arms appearance for feral harpies and bats mentioning that they had fingers. (PR#1456 by Stadler76)

Engine/Modding:
	Added 'NEGATIVE_ONE_LEGENDARY', 'NEGATIVE_TWO_MYTHICAL', and 'NEGATIVE_THREE_ZERO' as new SubspeciesSpawnRarity values (for subspecies which should be extremely rare).
	Added support for use of spaced 'ELSE IF' in conditional statements (although you should probably still continue to use 'ELSEIF' for style conformity).
	Added 'Sticker unlocks' button to the debug menu, which bypasses all clothing sticker requirements when turned on (for ease of testing clothing stickers).
	Added functionality for characters to gain category-locked perk points.
	Added 'TAIL_NEVER_SUTABLE_FOR_PENETRATION' BodyPartTag so that you can prevent prehensile tails from ever being used in sex.
	Added BodyPartTags 'FACE_VENOMOUS_TEETH' and 'FACE_VENOMOUS_TEETH_LUST', which causes the 'BITE' special attack to apply 'poisoned' or 'lust-poisoned' status effects to the target.

Gameplay:
	Added Nyan content up to the point where you can repeatedly go on weekend dates with her (and her mother).
	Added 'aristocrat' as a background choice during character creation.
	Reworked Pix's gym so that exercising no longer drains health, and instead applies a 'post-workout fatigue' status effect. Exercising in the gym now also grants progress towards unlocking physical perk points.
	You can now free your slaves by purchasing a Freedom Certification from Finch and then choosing the 'Set Free' action in your slave's management dialogue. If your slave likes you and you have a free guest room, you can have your slave become a guest after freeing them.
	You can now import characters as guests in the same way that you can import them as slaves. To do so, go to the waiting room in City Hall and use the 'Lodgers' action. Importing guests requires you to have a free guest room in Lilaya's mansion for them to move into.
	Snake-morphs now have venomous fangs, applying 'poisoned' to enemies which they bite in combat.

Body:
	The property of a vagina to birth live young or lay eggs can now be modified via the self-TF menu and/or by crafting TF potions.
	The orifice plasticity value of 'accommodating' now results in the orifice returning to 98% of its original tightness after being stretched, instead of 100%. (So the bottom 4 plasticity values now return to 100%, while the top 4 progressively return to lesser percentages.)
	Alligator tails are no longer marked as 'prehensile', and panther tails are marked as 'prehensile' (so that they can be used in sex if you have furry tail penetration turned on).
	Tails which are marked as suitable for penetration, but which are not prehensile, can now be used in sex so long as they are greater than 50% of the owner's height.
	
Sex:
	Characters in a 'performing oral' or 'missionary' slot in the 'lying down' sex position can now interact with the characters lying to either side of their target.
	Characters who are reverse face-sitting can now interact with characters who are scissoring the person whose face they are on.
	When using quick-sex, characters will no longer lose their vaginal virginity while tribbing with a clit that's not large enough to act as a pseudo penis.
	Characters with a positive desire towards the self-denial fetish no longer lose affection if they end sex without any orgasms, so long as they have been denied at least once (ending sex with no orgasms or denials still incurs an affection hit).

Other:
	Added indication of the covering's race to covering recolouring menus.
	Brax now starts with 150 essences, so he can use his pistol a lot more.
	Updated the minimap's night-time gradient effects.
	When searching for a partner in the club, subspecies are now ordered by race. You can also now select the race stage of your partner.
	The elemental dispel button is now displayed in both the interaction and management tabs.
	Changed maximum affection name from 'worships' to 'adores'.
	The drunk speech modifier now only takes affect starting at the 'drunk' level, instead of 'tipsy'.
	Body hair on furry morphs is now simply referred to as 'fur' instead of 'fur-like hair'.
	When choosing your name in character creation, and changing it at city hall, you can now set your masculine/andgrogynous/feminine name triplet, which causes your first name to change based on your femininity.
	Lyssieth now gains a lot of affection towards you after transforming you into a demon (will be retroactively applied if you are already a demon when loading into this version).
	Added 'orgasm prevention' enchantment for clothing that's either marked as a sex toy or which fits into the groin slot. While under this effect, characters can never gain more than 95 arousal, effectively preventing them from ever orgasming.
	Updated the icon for the 'desperate for sex' status effect.
	When purchasing or otherwise gaining ownership of a slave, you now gain keys to all of their equipped clothing which provides a key (such as their slave collar).
	If anal or lactation content is disabled, the enchantment menu will no longer show you secondary modifiers related to the anal orifice or lactation values.
	Kate will now let you use pregnancy testers on her during sex.
	The 'American tourist' background now grants doubled effects from eating burgers.
	
Bugs:
	Parsing and description fixes.
	Fixed issue where you could encounter egg-incubated offspring before they'd been laid and hatched.
	To fix an issue with dragons spawning in unintended places. Only subspecies which naturally spawn in Dominion or Submission will now be used as custom-order slaves from Helena and as generic sex partners (which are used in glory holes and a few other places).
	Fixed issue with breast stats not showing in the phone's stats menu if your cup size was less than AA-cups.
	Kate's covering recolouring options now correctly include lips, tongue, nipples, and anus. Also fixed incorrect covering options for when sending a slave to Kate.
	Custom-ordered slaves from Helena now have correct wing options available to them, and the colour of nipples/anus no longer resets when changing their human skin colouring.
	Fixed bug where horn transformations were missing from demon self-TF menu options.
	Fixed issue with the self-TF menu not working for recolouring slime fluids.
	Brax will now correctly have his weapons equipped when first encountering him in a new game.
	Fixed issue with Enforcer pepperball pistol's and rifle's 'Seven Rounds Rapid' and 'Mag Dump' moves throwing a background error.
	Fixed issue with NPCs sometimes having their home location set to seemingly-random tiles. This was mainly affecting Enforcer patrols (who had their home set to Candi's desk) and Wes and Elle (who had their home set to the HQ's waiting area).
	Fixed bug where error log could get spammed with null pointer exception warnings at the start of sex.
	Fixed issue where you needed both the 'Minx' and 'Object of desire' perks in order to seduce Wolfgang/Karl, instead of just one of the two.
	Fixed issue with feral demonic parts being referred to as 'feral Demonic-human'.
	Pregnant characters will no longer have their stomaches bulged from large penetrations.
	Fixed issue where human NPCs were spawning at a far higher frequency than what you set their spawn preference to be.
	Characters who are hidden during a sex scene (such as when you encounter and watch two of your slaves having sex) can no longer have their levels drained upon orgasm by any of the participants.
	Made fennec fox icon slightly smaller so that it fits in the icon background a little better.
	Fixed some issues with incorrect slime subspecies identification.
	Bunny and Loppy no longer act as though they didn't previously know what the other's genitals looked like the first time they're revealed in sex.
	Fixed incorrect descriptions for the chastity status effects (and increased lust resistance drain from -25 to -50 for the final stage).
	Fixed bug where very old save games would break when trying to load & save them in a newer version.
	Fixed bug where clothing would sometimes spawn with its sticker prefix applied twice and its color prefix missing.
	Fixed issue where changing Kay's makeup would change the player's makeup instead.
	Fixed issue where covering recolouring buttons would stop working after inspecting a character and then returning to a covering recolouring screen (such as when using the arcane makeup kit).
	Weapon descriptions now correctly list their special tags when you click on them in the inventory.
	Fixed some missing dialogue issues in the scenes with Wolfgang and Karl in 'The Rusty Collar'.
	Unemployed guests can no longer gain the 'stable mistress' job.
	Fixed bug where elementals would not have any of their status effects updated nor regenerate health/aura over time.
	Fixed issue with both lamia and melusine being tagged as the main race of snake-morphs, instead of just lamia.
	
----------------------

PATCH NOTES FOR v0.3.15

NoStepOnSnek's races:
	Added snake race, with subspecies of 'snake-morph' (bipedal snakes), 'lamia' (long-tailed snakes), and 'melusine' (long-tailed snakes with wings).		
	Added octopus race, with subspecies of 'octopus-morph' (cephalopod body).
	Added capybara race, with subspecies of capybara-morph (bipedal or quadrupedal body).
	Added 6 food/drink items: Boiled Eggs/Snake Oil for snakes, Shrimp Cocktail/Ink Vodka for octopuses, Chocolate Brownie/Chamomile Tea for capybaras.
	Added special attack 'Ink Cloud', unlocked by having an octopus face.

Contributions:
	Added support for multiple vagina or penis types per race in enchanted TF potion effects. (PR#1465 by Stadler76)
	Fixed issue where the combat moves of the player's elemental were reset. (by AceXP)
	Fixed softlock at the end of combat when fighting imps in Submission. (by AceXP)
	Improved performance by caching subspecies variables and only doing a recalculation when needed. (PR#1471 by AceXP)
	Fixed typo in 'Ear pull' blowjob action. (PR#1472 by darkofoc)
	Fixed issue where the appearance for feral legs was hardcoded and didn't take various leg configurations into account. (PR#1467 by Stadler76)
	Tidied up a lot of race code, and fixed issue where changing a character's tongueType (as part of changing face type) wouldn't resets its modifiers. Also added 'WING_SIZE_' as a parser prefix hook for WingSize enum values. (PR#1480 by Stadler76)
	Updated the tentacle-constrict icon. (by DSG)
	Made the tooltip fade-in animation toggleable via the existing 'Fade-In' game option. This fixes the bug where tooltips were appearing blank when using some versions of java to run the game. (PR#1449 by CognitiveMist)
	Improved damage calculations for special attacks. Added ability to set 'damageVariance' in modded combat moves. Added CombatMoveType POWER for use when defining special attacks instead of having to use ATTACK or SPELL. (PR#1473 by Stadler76)
	Fixed references to the player using their wings in several scenes when the player was in fact able to fly without their wings. (PR#1483 by Stadler76)
	Performance improvement and fixed issue with loading of book entries for subspecies without a bookEntries.xml file. (PR#1484 by AceXP)
	Fixed an oversight for mer-tailed and serpent-tailed non-ferals where the full leg description, complete with references to feet, was being incorrectly shown. (PR#1487 by Stadler76)
	Fixed graphical issues which arose when selecting very dark dye colors on items due to some stroke colors being set to CMYK black (#231f20) instead of RGB black (#000000). (PR#1488 by DSG)
	Fixed parsing errors, typos and minor issues in Nyan's updated quest content. (PR#1491 by AceXP)
	Added new icons for eagle-harpies and fennec-foxes. (by NeverLucky)
	Fixed bug where upon summoning your elemental for the first time, background errors would be thrown. (by AceXP)
	Made artwork file extension checking case insensitive. (PR#1448 by CognitiveMist)
	Improved performance and memory usage by implementing use of a single instance of the TransformerFactory, DocumentBuilderFactory and DocumentBuilder. (PR#1493 by AceXP)
	Fixed issue with wing types not being available in the enchantment menu, and also maximum penetration girth not being able to be selected. (by Stadler76)
	
DSG's Enforcer Item updates (PR#1490):
	Updated Enforcer item files: deleted outdated comments; fixed typos; updated weapon effects to be applied via effects element.
	Enforcer weapon effects are now applied on critical hits instead of by random chance.
	Pepperball rifle and pistol now have new special attacks of 'Mag Dump' and 'Seven Rounds Rapid', respectively.
	The Liquid Stun Gun's silly-mode effects have been moved into a new silly-mode variant of the weapon, which can be spawned via the debug menu's cheat spawn menu.
	Added a test Enforcer beret with no sticker requirements to the debug menu's cheat spawn menu.
	Updated Enforcer beret with some description text that was lost during sticker work.
	
DSG's race fixes:
	Race version 1.3:
		Removed face requirements from wyvern, drake, coatl, and ryu subspecies weighting for improved support for lesser morphs.
		Removed attribute scaling from the Breath Weapon special attack as it was already having damage boosted in damage calcuation, creating a "double-dip". Base damage is now fixed at 75.
		Removed ear requirement from coatls.
		Removed face TF from wyverns and drakes.
		Changed coatl tongue requirement to only require the BIFURCATED modifier.
		Improved flightlessness detection in drakes and ryus.
		Fixed incorrect year and formatting in the book entry for dragons.
		Fixed typo in bear vagina descriptions.
		Fixed gryphons spawning in with generic feathered wings instead of the correct wing type.
	Race version 1.31:
		Fixed three typoes in the dragon vagina TF description.
	Race version 1.32:
		Fixed similar typoes as 1.31 in the vagina TF descriptions for bears, ferrets, gryphons, otters, raccoons, sharks.
	Race version 1.33:
		Fixed formatting issue in the otter beverage effects description.
		Changed Breath Weapon calculation, base damage will now scale with spell damage bonuses. Starting damage is now 20. Having either a dragon torso or dragon face will increase starting damage to 50. Having both will increase starting damage to 75.
		Fixed feral coatls with a leg configuration of TAIL_LONG not being recongized as a coatl.
	Race version 1.34:
		Fixed dragon racialBody not having any tails listed
		Fixed gryphon racialBody not having tail feathers listed
		Added the "feathered" tail type to dragons
		Added a missing ARM_WINGS_LEATHERY tag to dragon arm-wings

Engine/Modding:
	Added parser prefix hooks for muscle, body size, and body shape enums (using 'MUSCLE_', 'BODY_SIZE_', and 'BODY_SHAPE', respectively).
	Added parser prefix hook for the DayPeriod enum (using 'DAY_PERIOD_').
	Eye type xml files now support the 'tags' element.
	Added argument to foot/feet parsing commands to ignore clothing when parsed during sex.
	Added 'CHASTITY' item tag, which makes clothing with this tag apply the new chastity effect to characters who equip it.
	Added an 'applicationLength' element to status effect mods. This enables you to define how long a custom status effect will be applied for if its application conditions are found to be true. If this 'applicationLength' is missing, the currently-used default value of -1 is used, so you don't need to refactor any of your status effect mod files to account for this change.
	Added RESTING_LUST as an attribute, so any modded items or effects can now influence this.
	Changed method signature for Sex methods: 'setTimesCummedInside()' and 'incrementTimesCummedInside()'.
	Added 'newSexType(SexParticipantType, SexAreaInterface, SexAreaInterface)' method to the sex class (at the very bottom of the class file) so that there's a way to generate SexType objects from the parser (via the 'sex' object).
	You can now define 'placeLocations' in subspecies xml files to allow for subspecies to spawn in specific place types. (See 'res/mods/innoxia/race/hyena/spotted.xml' for an annotated example.)
	You can now actually leave 'regionLocations' and 'worldLocations' elements in subspecies xml files blank without throwing errors, as the comments said you could.
	Added ability to define body hair availability to the bodyPart xml files: anus, arm, face, penis, and vagina.
	Added ability to define subspecies names based on their leg configuration. Refactoring old subspecies xml files is not needed. If you would like to make use of this functionality, see the 'res/mods/innoxia/race/hyena/spotted.xml' file.
	Also added ability to define subspecies silly-mode names. See the same file as above.
	Added 'HAIR_NATURAL_MANE' as a body part tag for defining HairTypes as being naturally styled into a mane.
	Added 'slotClothing(slot, coloured)' parsing command for parsing the name of a character's clothing.

Gameplay:
	Reworked Nyan's romance quest, which includes a new warehouse map and a new character. Nyan's post-quest dating content is half-finished, but will be completed for the next release.
	Added 'cougar-morph' as a subspecies of cat-morph. Requirements to be identified as a cougar are: non-patterned tan fur, muscles of at least 'muscular', and body size of at least 'average'.
	All chastity devices (cages and belt) now apply a new chastity status effect when equipped, which increases in intensity the longer the character continues wearing it.
	Added internal map to Slaver Alley's bounty hunter lodge, and renamed it to 'The Rusty Collar' tavern.
	Added public toilets to the Shopping Arcade, which you can use to wash yourself and/or use a gloryhole.

Items:
	Added: Women's trousers (feminine, leg slot, sold by Nyan).
	Added: Gemstone necklace (androgynous, neck/wrist slots, sold by Nyan).
	Added: Women's winter coat (feminine, over-torso slot, sold by Nyan).
	Bandada can now be worn in the head and hair slots, and supports pattern recolouring.
	Long-sleeved shirt is now unisex, and the colours of its buttons and tag can be changed.
	Added more colouring options to men's and women's watches.
	All glasses can now be displaced by being pulled up (onto forehead).
	Made the three brown clothing colours less saturated, so they look less orange and more brown than before. Also slightly desaturated the tan colour.
	Added 'dark desaturated brown' and 'desaturated tan' as new clothing colours.
	In clothing/weapon dye screens, standard colours for the selected item now have a slightly lighter border, and the tooltip for each colour reveals whether it's a standard colour or not.
	The 'Demonstone necklace' item is now sold by Vicky, not Nyan.

Sex:
	Added 'Stroke cock' as an ongoing self-action, which you can start/stop like other ongoing actions.
	Added 'foot worship' actions (performing oral on a partner's feet). Available in the slots: Performing oral (in positions Standing/Behind desk/All fours/Lying down), Reverse cowgirl (for non-taurs), Missionary (for non-taurs), Scissoring.
	Weighting of NPCs' choice to use foot actions is no longer partially based on the player character's fetishes, and is now only affected by the foot action content setting and whether the NPC at least likes the associated foot fetish.
	Added more information to NPCs' 'Desires' status effect tooltip when in sex, so that you can now see NPCs' foreplay and main sex preferences.
	Added 'Humping' sex slots to the 'Over desk' sex position.
	Characters can now use their serpent-tail lower body to perform all of the usual tail sex actions. Serpent-tail girth is based on hip size, while length starts at 500% of height.
	Stomach bulge descriptions are now appended when the penetration length inserted into a character's vagina or anus is greater than 12.5% of their height, instead of just when penetration lengths were detected as being uncomfortable.

Other:
	The five main horn types (curled, spiral, curved, swept-back, straight) are no longer limited to demons, and instead are generically available for all races who lack special horn types in the same way that feathered/leathery wings are.
	Hyena, panther, and demon eyes now have night vision.
	Rabbits, rats, and squirrels now correctly have plantigrade feet by default instead of digitgrade.
	Removed the 8-hour loiter action and added a 24-hour action.
	Resting lust increase from being vulnerable to an ongoing arcane storm has been reduced from 75 to 50.
	Hyena-morphs now correctly spawn with vertical pupils instead of round, and panther-morphs spawn with round pupils instead of vertical.
	You can now get your milk, cum, and girlcum recoloured by Kate at Succubi's Secrets, and you will no longer see covering recolouring options for parts you do not have (e.g. Horn covering colours will no be displayed if you have no horns).
	NPC surnames are now shown in their name tooltip.
	Updated home icons for Arthur, Zaranix, Desryth, and Helena.
	Slightly adjusted penetration girth brackets.
	Added indication of a serpent-tail's length in characters' body tooltip, and changed torso's 'Height' indication to 'Length' if the character is feral and their size is measured head-to-tail instead of how high they are.
	Serpent-tailed lower bodies can now have their length transformed (either from the self-TF menu or by enchanting food items which have the 'serpent tail' leg configuration transformation available to them, such as snake eggs).
	By default, only body parts belonging to mammal or bird races now support having pubic, facial, ass, and underarm hair.
	Feral snake subspecies now have more accurate body-to-tail length ratios, and by default are now closer to 2m in total length as a result.
	Added tentacle attributes to your phone's 'Body stats' screen and removed breast stats for if you're a feral which has no breasts.
	Added subspecies' status effect attributes to their encyclopedia pages.
	Nyan's Clothing Emporium is now open from 09:00-20:00 instead of 06:00-22:00.
	Traders will no longer always sell/buy unidentified clothing for 50 flames, and instead will offer a buy/sell price that's based on the item's unenchanted value. Also halved items' value reduction from having a 'jinxed' rarity.
	Added debug option to spawn an attacker of a defined race when on either a Submission tunnel tile or a Dominion alleyway or canal tile.

Bugs:
	Numerous parsing fixes.
	Fixed issue where characters could have their location set to coordinates outside of the map's edges.
	Fixed incorrect parsing in numerous footjob actions.
	Fixed rare issue where characters would have unintended sex preferences after changing position.
	The 'Frustrated' status effect is now correctly removed when the character under its effect orgasms.
	Fixed issue with Kruger and Kalahari not spawning correctly as lion-morphs (and retroactively reset their bodies to their correct forms when you load into this version).
	Fixed bug where numerous miscellaneous sex actions (including most of the sadistic actions and the 'pull hair/ears'-type actions) would never be available to use.
	The 'transformationName' element in vagina body part xml definitions now works correctly.
	Fixed bug where Helena would repeat conversation topics before you'd seen all of them.
	Fixed issue with several incorrectly-gendered cock names (e.g. A male fox's cock being called a 'vixen-cock').
	Fixed very rare bug where the game could randomly freeze for a turn when removing certain items of clothing.
	Fixed issue where 'Present pussy' positioning action was available in gloryhole scenes even if you didn't have a vagina.
	The size of the preview image when dying clothing and weapons now correctly fits into the tooltip's width.
	Fixed incorrect colouring of some status effect icons (such as the icons for the smoking effects).
	Fixed minor bug where ordering of attributes in modded race tooltips would be random.
	Fixed issue where tentacle count was not correctly linked to leg count.
	Fixed incorrect descriptions of height and serpent-tail length for feral characters.
	Fixed issue where transforming into a feral wouldn't apply the correct leg configuration changes, which was leaving characters with tails where they should have had them removed.
	Fixed bug where feral attributes of modded races were not being loaded correctly.
	Fixed minor issue with feral Coatl not being described as serpents in some places.
	Fixed issue with unintended subspecies spawning in the stocks at slaver alley (such as dragons).
	Changing pupil and sclera colour in Succubi's Secrets should now work correctly.
	Fixed issue where hair type was not being checked as being suitable for pulling or not in hair-pulling sex actions.
	Fixed issue where non-harpy offspring could be encountered in the harpy nests.
	Tail length percentages in the self-TF menu should now always correctly increment by 5%, instead of sometimes jumping by 6%.
	Fixed issue where rat-penises were no longer spawning in with pale pink skin by default.
	Fixed issue with feral parts on a half-demon (such as on taurs) always being referred so as being of a 'demonic-horse', instead of the half-demon's correct subspecies.
	Fixed bug where name of nipples was being shown instead of name of crotch nipples, and added more randomly-generated descriptors to the list which nipples use.

----------------------

PATCH NOTES FOR v0.3.13

Contributors:
	Dragon breath attack is now unlocked by the character's race being identified as 'dragon', not by having a dragon torso. (by DSG)
	Fixed issue with the dragon subspecies 'Coatl' not being detected correctly. (by Stadler)
	Fixed bug where feral characters would spawn with crotch-boobs, even if crotch-boob row count was defined as 0. (by Stadler)

Engine/Modding:
	Added parser hooks to penetration, orifice, and tongue modifiers (using prefixes 'PENETRATION_MODIFIER_', 'ORIFICE_MODIFIER_', and 'TONGUE_MODIFIER_' respectively).
	Added support in racialBody xml files for setting 'breastCrotchType' to NONE for races you want to never spawn with crotch-boobs.

Other:
	Characters no longer have their cum & girlcum automatically gain the 'musky' modifier when changing into a non-bipedal leg configuration. (Centaurs still have this modifier by default.)
	Sharks and all dragon subspecies will no longer spawn with crotch-boobs.
	Removed restrictive minimum and maximum limitations for insect wing size.
	Ralph no longer sells Impish Brew (you can still buy it from Roxy).

Bugs:
	Racial food items which have more than one torso type associated with them now have access to those torso types in the enchantment menu.
	Fixed dragon's 'Breath weapon' special attack dealing 0 damage.
	Fixed some minor issues with NPCs spawned as a dragon subspecies having the odd part assigned incorrectly.
	Fixed bug where the penis slot would not accept any clothing if a character lacked a penis, causing strapons to be impossible to equip.

----------------------

PATCH NOTES FOR v0.3.12

Contributors:
	Added variations of starting demonstone damage type based on your birth month, and correct some descriptions during the prologue related to this. (PR#1409 by Rfpnj)
	Fixed bug where the 'Dye & reforge all (stack)' action would not consume reforge hammers. (by AceXP)
	Fixed bug where 'Unequip all' would inadvertently unequip milking pumps, which would end up with them being added to your inventory. (by AceXP)
	Editing your character's description in their save file will now display that description in the in-game selfie screen. (PR#1411 by aDrunkLittleDerp)
	Fixed issue with incorrect anus description for elementals (with help from PR#1412 by AceXP).
	Fixed parser command 'glow' to work without a defined colour, as well as for rainbow colours. (PR#1439 by CognitiveMist)
	Typo fix in bread roll description. (PR#1414 by aDrunkLittleDerp)
	Added the option for a slave to be mute to Helena's custom slave shop and removed tongue recolouring from the Hair options tab. (PR#1416 by AceXP)
	Characters with the NON_CON_DOM fetish will now gain lust when having sex with someone that is resisting. (PR#1417 by AceXP)
	Slaves in the stocks at Slaver Alley without a vagina will no longer have vaginal sex events generated for them. Also fixed these slaves' descriptions and the issue where they would always have all permissions granted. (PR#1426 by AceXP)
	Added checks for fertility pills, including broodmother. Roxy now sells broodmother pills and random NPCs may sometimes be carrying them. Ralph and Lilaya now react to broodmother pills in the same way as fertility pills. Fixed incorrect colour descriptions of fertility pills in several places. (PR#1422 by AceXP)
	Fixed issue where hair length, breast size, ass size, and hip size had no tolerance so that post-combat forced TFs alternated between too big and too small. (PR#1334 by Stadler76)
	Fixed typo in phoenix-harpy description and tidied up parts of the code in UtilText.java. (PR#1336 by Stadler76)
	Fixed some instances of incorrect unit parsing. (PR#1321 by NoStepOnSneks)
	Fixed a bug where if a clothing item to be equipped had multiple occurrences, equipping this item would lead to bugs when the next occurrence of the item was to be equipped. (PR#1419 by Deboucher & AceXP)
	Fixed the bug where clicking on an equipped item while enchanting during a trading session would give you full access to the inventory of the trader, allowing you to take all their equipped items and the items in their inventory. (PR#1420 by AxeXP)
	Fixed issue with milking rooms not being able to support 8 slaves, maids gathering on the player's tile when loitering in the corridors of Lilaya's home, and the 'well rested' status effect no being applied correctly. (PR#1425 by AceXP)
	Enchantment recipes can now be applied to weapons that already have enchantments. (PR#1423 by AceXP)
	Updated github build tutorial. (PR#1323 by LjyiH)
	Fixed missing verbs in several files. (PR#1291 by TadUnlikely)
	Fixed incorrect dialogue scene titles when getting tattoos in Kate's shop, incorrect description of how much cum was expelled during orgasm when performing a double creampie orgasm action, and a reference to ass instead of breast in nipple-fingering actions. (by AceXP)
	Fixed a bug where having an elemental in a feral form would cause the the left and right sidebar to go blank. (PR#1457 by AceXP)
	Prevented pregnant slimes without a vagina from transforming back to flesh, as the birthing scenes only account for characters with a vagina. (PR#1459 by AceXP)
	Fixed issue where Sean could not be challenged a second time if you backed out and changed your mind about fighting him. Also fixed some incorrect clothing descriptions and missing text. (PR#1458 by AceXP)
	Added support for defining feral face description in face modding xml files. (PR#1452 by Stadler76)
	Added 'Poncho' clothing item. (Unisex, over-torso slot, sold by Nyan.) (by NoStepOnSnek)
	
DSG's race contributions:
	Added 7 new races: Sharks, Bears, Dragons, Ferrets, Gryphons, Otters, and Raccoons.
	Added 1 subspecies for each of these new races, except for the dragon race, which has the subspecies: Coatl, Ryu, Dragon, Drake, and Wyvern.
	Added 18 new consumable items, consisting of a drink (attribute) & food item (transformative) for each of the 7 new races, with dragons having an extra 2 variants of their drink item and 2 extra variants of their food item.
	Added 12 new colours related to the new races added.
	Added 7 new combat moves for the new races: 'Charging Bite' (sharks), 'Five Claw Strike' (bears), 'Breath Weapon' (dragons), 'War Dance' (ferrets), 'Hunting Call' (gryphons), 'Tail Slap' (otters), and 'Cornered Beast' (raccoons).

Engine/Modding:
	Made some slight improvements to the documentation of the xml files related to race modding.
	Added support for wing types to have a defined minimum and maximum size (see the 'res/mods/innoxia/race/hyena/unused_bodyParts/wing.xml' for the commented example).
	Added comments for the imageName elements in 'res/mods/innoxia/items/items/race/hyena_bone_crunchers.xml'.
	Choosing to not define any covering modifiers or patterns in coveringType mods is now correctly handled without throwing background errors.
	Leaving the 'backgroundName' element empty or not including it in subspecies xml mod files is now correctly handled and uses the default race background (as was implied it should in the comments).
	Added elements in the 'racialBody.xml' file for defining male and female hip sizes ('maleHipSize' and 'femaleHipSize').
	Added parsing hook to BodyPartTag (using the prefix 'BODY_PART_TAG_').
	Added ColourTags, which can be added to modded colours to have them be automatically added to the game's covering colour lists.
	Added setCovering() to Body class to make the setting of coverings easier in race mods. (See 'applySubspeciesChanges' element in lion.xml for an example on this being used.)
	You can now leave the half-demon name elements empty in subspecies xml files (in which case the game will automatically generate a generic half-demon name for your subspecies).
	Added support for a 'displaySize' attribute to the 'iconName' element in subspecies xml files, allowing you to define the resizing percentage of your icon image.
	Added 'coveringIconColour' element for modded colours, allowing you to define the colour to use a different colour for covering icons than its usual colour for text.

Gameplay:
	Added a separate variant of the aquatic status effects for characters of an aquatic race who have the leg configuration 'TAIL'.
	Added ability to recolour cum, girlcum, and milk in the self-TF menu.
	Minimum size for a clitoris to be used as a psuedo-penis has been increased from 1cm to 5cm.
	Split cat-morph race into cat-morph and panther-morph. Removed cat-morph's 'panther face' TF option. Tigers, lions, leopards, and snow leopards are now classed as panther-morphs.
	If a character has the cat-morph's 'panther face', their cat-morph body parts will be converted into panther-morph parts when loading into this version.
	Added 'Deep Roar' and 'Panther's Delight' consumable items for the new panther-morph race.

Other:
	Improved sorting of subspecies in several menus.
	Updated spawn locations of all subspecies.
	Altered the names of the reindeer and centaur books.
	Added some more global NPC transformation debug buttons (in Misc. category).
	Added labourer outfits, so reindeer overseers will no longer spawn with completely random outfits.
	Slightly adjusted the default colours of the leather belt.
	Diamond necklaces will no longer spawn as a random item in Dominion's alleyways, canal tiles, or in the crates in the Supplier Depot.
	Characters with the TAIL_LONG leg configuration now gain access to the 'tail swipe' combat move.

Body:
	Added ROUGH as a covering modifier.
	Added TAPERED as a tongue modifier.
	Added REPTILIAN and AMPHIBIAN foot types.
	Added BodyPartTags TORSO_DORSAL_FIN, TAIL_TYPE_SCALES, THERMAL_VISION, and ALLOWS_FLIGHT.
	
Sex:
	NPCs now have the chance to decide to initiate penetration using a clitoris that's large enough to act as a pseudo-penis.

Bugs:
	Fixed bug where characters of a modded race would show as 'human' after loading a game.
	Fixed non-centred alignment and uneven circle dimensions of race & item backgrounds.
	Encyclopedia information for modded races should now load and display correctly.
	Fixed issue with the tile's default dialogue being shown alongside the intended dialogue when refusing a partner's offer of sex in the nightclub.
	Fixed issue where declining sex in a nightclub partner's apartment would lead into the nightclub's toilets dialogue instead of Dominion boulevard dialogue.
	The game no longer autosaves when following or taking a nightclub partner home, as loading the autosave which was generated at that point would result in that NPC being unintentionally deleted. Instead the autosave is generated after leaving the partner.
	Fixed bug where nightclub partners would not be saved if you followed them home and then refused sex, despite the tooltip indicating otherwise.
	Fixed huge amount of background errors being thrown whenever you changed any of your furry preferences (which was causing that preference screen to lag a lot).
	Fixed issue with race books not showing up in the library.
	Added handling for automatic birthing of nipple-incubation eggs when a character transforms into a feral form which lacks breasts.
	Fixed issue where litters birthed by NPCs would always have the same birth date as their conception date.
	Fixed issue where background errors would be thrown if a generic sex event generated a half-demon character.
	Fixed issue where NPCs with eggs implanted in them would never lay the eggs if you saved & loaded the game while they were in the 'completed' stage of incubation.
	Removed incorrect reference to going to consulting Lilaya when having eggs implanted inside of you, and replaced it with a hint on having to access your phone's menu in order to lay them.
	Enchanting the item 'Biojuice Canister' now correctly gives you just the option to create a slime-reversion elixir, instead of the full racial options that other standard racial TF items have access to.
	Fixed image position and alignment in combat move tooltips.
	Fixed issue where milking pumps and spider webbing seals could spawn as generic clothing on randomly-generated NPCs.
	Fixed spotted & striped hyenas not having correct plural names for their feral forms.
	Fixed issue where TF potions with a TF type that's been removed from the game would throw background errors when trying to use it.
	Fixed parsing errors when eating the hyena food item 'Bone Crunchers'.
	Fixed reference to feral characters having feet when they had a tail lower body type.
	Fixed a couple of issues that were causing modded status effects to not work.
	Fixed issue where loading a previously saved game would sometimes show parsing errors on the initial dialogue page (for example, in the entrance tile to Slaver Alley).
	Fixed spam of warnings about getFeralAttributes() returning null every time you loaded the game as a feral character.

----------------------

PATCH NOTES FOR v0.3.10

Contributors:
	Fixed issue where NPC speech would sometimes have errors in it. (PR#1415 by AceXP)
	Added a unique icon for the 'dazed' combat status effect. (by DSG)

Engine:
	Added modding support for items to be defined as being able to be enchanted into new items, and support for a background to be added to item images, as well as size and rotation definitions. (See 'res/items/innoxia/race/horse_equine_cider.xml' for an example.)
	Added support for nesting folders inside mod folders (so mod makers can more easily categorise mod files within their directories).
	Improved performance of status effect conditional checks, which should have considerably improved the time it takes to end a turn in games with many saved NPCs.
	Added 'tags' field to status effect modding, allowing (some) ItemTags and their effects to be applied to modded status effects. (See the 'res/mods/innoxia/statusEffects/set_template.xml' file for an example.)
	Added parsing commands for clitoris diameter and circumference.
	Improved handling of body covering types in the code.
	Added full mechanics support for all other leg configuration types (serpent-tail, fish-tail, arachnid, cephalopod, avian). You can test these lower body types by using the debug TF menu to give yourself the demonic leg types which support this.
	Added 'aquatic' race definition and land/water tile definitions, so that aquatic races have beneficial/detrimental status effects applied when they are in a water/land tile respectively. Tile land/water status and danger status is now displayed at the top-right of the UI.
	Added full support for spinnerets, which will be granted by spider tails and spider 'arachnid' leg configurations. Spinnerets can be used as sexual orifices, and also grant several web-spinning sex actions, along with a special combat move.
	Added full support for penises and clitorises to be ovipositors, by means of giving them a modifier (via TF potion or self-TF menu). Characters with an egg-laying vagina which has been impregnated can use an ovipositor penis/clit to lay the fertilised eggs in vaginas, anuses, nipples, and mouths.
	Cephalopod lower bodies now support tentacles as penetrative objects (like tails) and grant a special combat move.
	Added support for combat move modding. (See 'res/mods/innoxia/combatMove' and 'res/combatMove' for examples.)
	Added support for fully-feral bodies. (There is currently no way to obtain a feral body, but the underlying code is ready for future content.)
	Added full support for race modding. (See 'res/mods/innoxia/race' for an example.)
	
Gameplay:
	Added 'darkness' mechanic. Darkness status effect gets applied when a character is located in a map tile which is not illuminated. This status effect can be negated by having animal morph eyes which grant night vision, bat ears (which grant echo location), a body made of fire, mastery of fire spells, or an equipped piece of clothing/weapon which counteracts darkness (night vision goggles or the flashlight).
	Increased upper cap of base unarmed damage from 20 to 50.
	Added 'hyena' race with 'spotted hyena' and 'striped hyena' as its two subspecies. Added related 'Bone Crushers' food item and 'Workout Power' drink item.
	
Items:
	Added weapon: 'Flashlight'. Sold by Ralph, illuminates dark areas when equipped.
	Improved icons for all racial attribute drinks (such as Equine Cider, Canine Crush, Wolf Whiskey, etc.), and moved all of them out from the code into the external 'res/items/innoxia/race' folder.
	Moved all racial food items out from the code into the external 'res/items/innoxia/race' folder.
	The 'Angel's Tears' item has been considerably buffed and can no longer be naturally found in-game (it will be added back into the game later on).
	Made 'tabi socks' unisex.
	Most racial transformative food items now additionally restore 10% health when consumed.

Body:
	Added a transformable value for tail length, expressed as a percentage of the tail owner's height (minimum value is 5%, maximum is 250%). It can be modified via the self-transformation menu (for demons or slimes), or via a new potion enchantment option.
	If a tail's girth is the same as the default value for its type, then changing the tail type will reset the girth to the new tail's default girth. The same happens with tail length.
	Alligator-morph body hair is now coarse hair (the same as their head hair). It is always absent on alligator-morphs by default if you have your 'Scaly Hair' option off.
	Added more options to change the colour of your elemental's body coverings.
	Fixed issue where face type would always use the same covering as torso type.
	Increased maximum breast and crotch-boob row counts from 5 to 6.
	Slightly adjusted clitoris size category values to make them mroe in-line with penis size values, and reduced maximum length from 125cm to 100cm (so that it's the same as penis length).

Sex:
	Fixed several parsing errors and incorrect descriptions of several sex actions (mainly tail-asshole and tail-vagina actions).

Other:
	Ralph now sells modded weapons which have been given the tag 'SOLD_BY_RALPH'.
	Slaves now enjoy the prostitute job if they have the 'nymphomanic' trait active, instead of if they have the cum addict fetish.
	The cum-inflation status effects for a character's breasts are now triggered by either breasts or crotch-boobs being inflated by cum.
	Horn adn wing types will no longer have random ordering in the self-TF menu's options.

Bugs:
	Fixed issue where using the 'Quit' button in the main menu would sometimes fail to close the game's background java process.
	Fixed bug where summoning your elemental for the first time in a new game wouldn't work.
	Taking a thorough shower in your room's bathroom now correctly applies the 'Recently showered' status effect.
	Fixed bug in conditional parser where identical if statements that each return 'true' would return the last encountered block instead of the first.
	Elementals now correctly return to their passive form after successfully escaping from combat.
	Hair clothing is now correctly unequipped when hair length is set to 0.
	In the 'Witch's Seal' sex scene with cultists, the character who is sealed can no longer use orgasm-locking actions (i.e. 'leg-lock', 'hug-lock', etc.).
	Fixed issue with some NPCs spawning with metallic-coloured shirts.
	Fixed issue where tail length decrease button would continue to work when greyed-out.
	Orgasm actions which direct cum onto a partner's groin will now correctly dirty their vagina/penis inventory slots.
	Fixed issue with 'hoof-kick' attack's critical hit logic not working correctly.
	'Martial artist' perk now correctly increases base unarmed damage, instead of modifying the damage in the same manner as the 'unarmed damage' attribute's calculation.

----------------------

PATCH NOTES FOR v0.3.9.9

Gameplay:
	Starting Claire's teleportation side-quest now requires you to have first completed the 'Slime Queen' side quest. (As I felt as though it was a little out of character for the Enforcers to let a stranger see the teleportation pads.)

Items:
	(For Clothing Modding) If multiple stickers in one sticker category are set to be the default sticker, one of these default stickers is now chosen at random to be used for an item of clothing, instead of always the last defined default sticker.
	Made the shoulder strap on the 'ragged chest wrap' a sticker option.
	'Impish Brew' now grants +25 corruption to potion effects, instead of +50.
	Added ability to enchant clothing with vagina and penis addition and removal effects.

Sex:
	You can no longer 'Encourage creampie' or 'Encourage pullout' when spectating in a 'hidden' position (such as when you watch your slaves having sex in the alleyway or hallway encounters).
	You can now use level drain on orgasming characters while in a spectator slot.
	Added interactions in the 'Sitting' position between the 'Sitting in lap' slot and the 'Between legs' slot.
	Added interactions in the 'Over Desk' position between the 'Lying back' slot and the 'Bent over' slot.
	Added kissing and groping interactions between dominant and submissive standing characters in the 'Standing' sex position.

Other:
	The output of all parsing commands embedded within speech should now be correctly modified by any speech-altering effects (such as a slovenly character pronouncing 'her' as ''er').
	Transformative potions which turn a character's lower body into a taur now correctly transform all of the body parts which are affected (all parts below the waist) into their default animal counterpart states.
	Added transformation actions to alleyway prostitutes' post-combat victory scene.
	Added pregnancy reactions to Murk's greeting dialogue while in Epona's tile.
	Standardised sorting of all racial transformation options by their race name.
	Half-demons no longer use the same outfit generation as dark alleyway demons, and dark alleyway demons now have a 5% chance to spawn with demon daggers instead of 50%.
	The 'Enforcer HQ' tile is no longer considered to be dangerous during an arcane storm.
	Increased the chance of the street encounter in which Wes's quest starts from 10% to 50%.

Bugs:
	Typo and parsing fixes.
	Fixed issues with sex scenes at Epona's stall in the Gambling Den being treated as public sex.
	Fixed bug where the Rat Warrens content would break if rat-morph Subspecies preferences were set to 'human'.
	Fixed bug where accessing the positioning menu in the prologue sex scene would reset all of the previous sex dialogue.
	Fixed issue with there being two 'miss' parsing commands.
	New slaves will now correctly start with all default job settings and permissions selected.
	Fixed harpy attacker NPC descriptions not changing when you become friends with them or enslave them.
	Fixed issue with the 'slovenly' character speech modification sometimes breaking parsing commands.
	Fixed Murk's and Lyssieth's special dirty talk text not being parsed as speech.
	Choosing to dominantly fuck Murk in Epona's tile (after completing Axel's quest) should now start with both of you in the intended positions.
	Fixed bug where slave interaction scenes in alleyways or Lilaya's corridor would sometimes throw background errors and not initialise correctly.
	The Spa tile is now correctly immune to arcane storm effects.
	Fixed issue with enslavement of friendly NPCs describing them as though they'd just been defeated in combat.
	Exiting Lyssieth's palace now correctly places you in the cavern tile instead of the palace gate tile.
	Fixed existing Patrol Enforcers in Dominion wearing 'contractor' stab-proof vests instead of Enforcer ones.
	If foot, anal, lactation, or non-con settings are turned off, NPCs will no longer have the related fetishes or fetish desires.
	If non-con is disabled, the related fetishes are now correctly hidden from the fetish list and fetish altering potion effects.
	Fixed NPCs being described as being in the 'holding cell' in their contacts page tooltip.
	Fixed issue where attributes derived from clothing could sometimes be duplicated or persist after the clothing's removal.
	Fixed issue where equipping transformative clothing onto demons or half-demons would sometimes spam the event log with messages.
	Dominant partners in the Watering Hole will no longer spawn with the 'submissive' fetish, and likewise Submissive partners will no longer spawn with the 'dominant' fetish.
	Fixed background errors being thrown if you decided to spam-click the 'New Game' action.
	Added a 'no preference' option to Scarlett's sex scene (where you act as her servant in Helena's nest), so that if you have no areas available for her to fuck, you no longer get stuck in that scene.
	Added actions to exit Helena's apartment at the entrance tile (for if you somehow manage to get stuck in there).
	Elementals now have the correct arcane storm status effect applied to them.
	Fixed bug where you could swap position with Murk's milkers during sex with them.

----------------------

PATCH NOTES FOR v0.3.9.8

Contributors:
	Fixed issue where changing content options at the start of new character creation would throw background errors, causing the UI to become unresponsive. (by AceXP)
	Fixed issue where fluid addiction status effect tooltip descriptions would display 'demonic horse fluid' instead of 'demonic fluid'. (by AceXP)
	Fixed bug where the defined horse-morph names in Name.java were never being used. (by Rydelfox)
	Several parsing and typo fixes. (by AceXP)
	Fixed issue where you would return to an incorrect dialogue scene when leaving inventory management in a friendly occupant's apartment. (PR#1394 by AceXP)
	Typo fixes in the Rat Warrens. (Pr#1400 by aDrunkLittleDerp)
	While carrying an arcane makeup set, characters will now reapply heavy lipstick if it was worn off during sex. (PR#1403 by CognitiveMist)
	Fixed parser errors in vagina reveal descriptions. (PR#1404 by AceXP)
	Enable loading of patterns from the res/mods folder. (PR#1405 by AceXP)
	Fixed bug where five minutes passed, instead of twenty-five, when selling yourself as a submissive partner in Angel's Kiss. (PR#1406 by void-weaver)
	Fixed bug where Sean's fight scene wouldn't initialise correctly. (PR#1407 by void-weaver)
	Fixed bug where if you used an item from an NPC's inventory it would be described as though the NPC was using the item. (PR#1408)

DSG's Enforcer Uniform Update:
	Added sticker system support, consolidated all extant variants of the Enforcer stabvest, coat, waistcoat, beret, peaked cap, and bowler hat into their respective items.
	Added the following sticker assets that did not already exist in some form in the game: Combat Diver Badge, Commissioner Cap Badge, Commissioner/Deputy Commissioner Visor/Crown Oak Leaves, Commissioner Aiguillette, Elis Cap Badge, Thinis Cap Badge, Itza'aak Cap Badge, Lyonesse Cap Badge.
	Detailed buttons added to the Enforcer coat and waistcoat.
	Fixes and standardization of ribbon racks and name plates.
	Hand optimization of almost all vectorized text.
	Added the 'Contractor's' variant to the stab vest and plate carrier.
	
DSG's Enforcer outfit update:
	Added sticker and pattern support.
	Renamed conditionals to be more reader friendly.
	Changed comments to be more clear.
	Removed berets from the Patrol Service Uniform.
	Possibly fixed bugs related to headgear spawning on Enforcers with the wrong colors and no headgear spawning on Enforcers entirely.

Engine:
	Added ItemTags for defining items, clothing, and weapons as being restricted or illegal, causing them to be unable to be sold to merchants and confiscated by Enforcers.
	Added mod support for defining clothing 'stickers', which apply cosmetic changes to clothing items. (See 'res/mods/innoxia/items/clothing/rentalMommy/rental_mommy.xml' for a fully documented example of how to define them.)

Gameplay:
	Added two new Enforcer characters and a new quest involving them, all of which has been designed by DSG. The start of this quest will randomly trigger in Dominion's street tiles under the following conditions: no arcane storm; main quest is past Brax's section; over 5 days have passed since completing the 'Angry Harpies' quest; time is 17:00-21:00.
	Enforcers in the 'alleyway Enforcer encounters' will now confiscate illegal items, and arrest you if they find that you're carrying highly illegal items.

Items:
	Added sticker support to the 'rental mommy' and 'rental daddy' T-shirts.
	'Biojuice Canisters' and 'Glowing Mushrooms' are now tagged as restricted items.
	'Demon's Dagger' (no longer sold by Vicky) and all of the Enforcer weapons are now tagged as either illegal (Enforcers will confiscate them) or highly illegal (Enforcers will arrest you).
	All Enforcer clothing is now tagged as illegal (Enforcers will confiscate them).
	
Other:
	Slightly altered description of 'cynical' personality trait to differentiate it from 'selfish'.
	Items and weapons will now correctly display ItemTag descriptions in their tooltips.
	Roxy now buys weapons as well as items and clothing. Her buy modifier has been reduced from 0.4 to 0.3 (meaning she will now only give you 30% of an item's value).
	Sean now correctly wears an Enforcer patrol uniform instead of a dress uniform.

Bugs:
	Parsing fixes.
	Updated example links in xml modding files to point to the correct files.
	Fixed bug where you could get stuck in Brax's office after resolving the part of the main quest which involves him.
	Fixed issue with the cheat guns' 'mag dump' combat move being automatically removed after selecting it.
	Fixed descriptions of putting kitty panties on/off being inverted.
	Fixed bug where weapons could show incorrect image previews in the dye screen. (The 'Demon's Dagger' was suffering from this.)

----------------------

PATCH NOTES FOR v0.3.9.4

Contributors:
	Added an encounter in Dominion's alleyways and Lilaya's home's corridors where you stumble upon two of your slaves having sex with one another.
	 To trigger, you need your slaves to have the appropriate outside/house freedom and sex permissions, and the one initiating sex needs to have not had sex for at least 4 hours and to be attracted to the other. (by PoyntFury)
	Improved String-matching utility methods and dynamically generated ColorListPreset classes. (PR#1368 by CognitiveMist)
	Fixed bug where sometimes multiple-partner sex would break upon orgasm. (by CognitiveMist)
	Added 'broodmother pill', which doubles offspring conceived during its effect. (Usage dialogue written by PoyntFury)
	Fixed a bug where having multiple arm pairs allowed an all-out strike with a 2-handed weapons. (PR#1384 by AceXP)
	Added average penis girth in the Encyclopedia information on races. (PR#1385 by AceXP)
	Prevented any succubus/incubus alleyway attackers from spawning with the 'Prude' trait, as it doesn't fit them. (PR#1386 by AceXP)
	Fixed issue where 'Arcane impotence' was being applied when arcane was lower than 15, instead of lower than 10 as it should have been. (PR#1388 by AceXP)
	Standardized all encounters to override getDialogues() instead of accepting Util.newHashMapOfValues() as a parameter. (PR#1389 by DSG)
	Added a new 'limited' option for the bypass sex action content setting, which allows you to perform sex actions of one corruption level higher than your current corruption. (PR#1391 by AceXP)
	Added 'wet wipes' item, which cleans the target's dirty inventory slots when used. (by DSG)
	Added 'peach' as a silly-mode item, sold by Ralph. (Adapted from PR#339 by Rfpnj)
	Added variation of what your starter spell is based on your character's birth month (fireball, slam, ice shard, or poison cloud). (PR#966 by Rfpnj)
	
Engine:
	Added modding support for items. You can find a fully-documented example in 'res/items/innoxia/pills/fertility.xml'. Item modding will be expanded at a later date to support enchantments, but for now, the modding framework should be enough for most uses.
	Converted Combat from an Enum to a class, which can now be accessed via the parser using the command 'combat'.

Rat Warrens:
	Fixed bug where Murk would always use the 'normal' dom pace instead of being rough.
	Fixed several instances of Murk's sex scenes ending with an action named 'Milking room' with no tooltip description.
	Fixed bug where Murk would fuck you without first taking out your pussy pump.
	Fixed issue with missing dialogue node when having sex with Murk in the Gambling Den.
	THe 'Free captives' action in the milking room is now correctly disabled once you've discovered that the milkers cannot be freed.
	Filled in all placeholder dialogue for both Vengar's and Murk's post-quest-completion scenes in the Gambling Den.
	Murk's name now remains as 'Murk' after feminising him in the post-quest gambling den content.

Items:
	Reduced rarity of crafted 'Fetish Endowment' potions from legendary to epic.

Sex:
	NPCs will no longer feel the urgent need to expose masculine characters' nipples during sex.
	You can no longer deny your partner's orgasm in the 'glory hole' sex position.
	Fixed bug where your sealed clothing wouldn't be displaced at the start of the Enforcer's 'strip search' sex scene.
	Added positioning requests to the 'glory hole' sex position for when you're dominantly using it, so you can ask the person on the other side to push their pussy or ass up against the hole to be fucked.
	Blocked 'Offer X' and 'Request X' actions in the 'glory hole' sex position (as they didn't really work due to the position's limitations).
	NPCs will now only self-use an item type once in sex (so you no longer have to repeatedly use pills on an NPC who wants to use the opposite type of pill).
	Added an 'Automatic stripping' content option (in the 'sex' property category), which makes it so that all characters start naked in each sex scene. This is disabled by default.
	Sex scenes in which characters automatically start naked no longer remove their piercings.
	Fixed issue with NPCs self-using breeder pills in illogical situations.
	Lowered corruption requirements for most positioning actions.

Slavery:
	Added 'Save Virginity' as a generic permission for slaves, which is enabled by default.
	Slightly improved wording of slave sex interactions in the log.
	Reduced the chance for slaves to have the 'bonding' event with one another.
	Added filtering options for the 'Occupancy ledger' in the Office room. You can filter events by their type and by slaves involved.

Other:
	Enforcer encounters now have a cooldown of four hours before they can be randomly encountered again.
	Characters in the 'lying down' sex slot can now kiss/suckle a character's breasts if they are in the 'cowgirl' sex slot.
	The 'American tourist' occupation now only parses the main dialogue screen when converting spelling to American English (as it was causing some lag when trying to parse everything).
	Elementals are now always treated as having all their body parts pierced (due to their transformative abilities).
	Split up Elemental dialogue into 'Interactions' and 'Management' tabs, and added a management option 'Self-clean' to set whether or not your elemental automatically cleans dirty fluids from their body/clothes (enabled by default).
	Elementals now spawn at maximum affection towards their summoner (this will be retroactively applied to your Elemental when loading into this version).
	NPCs who do not have the martial artist perk and who have a main weapon equipped and no offhand weapon equipped will now be far less likely to use the 'offhand strike' attack.
	The SWORD Enforcers in the Enforcer Warehouse (in Claire's teleportation quest) now prefer to attack in combat rather than teasing.
	If you have anal content disabled, the 'buttslut' fetish is no longer a requirement for unlocking the 'lusty maiden' fetish.
	You can no longer encounter the same person in the nightclub more than once per night.
	Moved 'Post-sex clothing replacement' property category from 'gameplay' to 'sex'.
	You can no longer give Bunny or Loppy items during sex.
	Added pregnancy reactions for if you manage to impregnate Bunny and Loppy, and slightly improved the flow of dialogue when entering their rooms.
	Added two new upgrades to the 'Soothing Waters' spell, which cause it to clean the target's body & clothing and wash out fluids from their orifices.
	Added 'Head pat' action to Nyan's romance actions.
	Added 'naive' and 'cynical' personality traits. (They are like the other core traits in that they are mostly for roleplaying purposes and will have some limited dialogue variations throughout the game.)
	Updated 'Enforcer HQ' map.

Bugs:
	Numerous parsing and typo fixes.
	Fixed issue with slaves not being correctly identified as being able to ambush you in Dominion even if you gave them the right permissions.
	Fixed issue where slaves would never jump you for sex in alleyways that already had a persistent character present in them.
	Slaves being held in Slavery Administration will no longer generate slave-interaction events with other slaves.
	Silly-mode items are no longer tracked by the Encyclopedia (so that players doing normal playthroughs will not be confused as to why some items are unobtainable).
	Fixed minor issue with the display of clothing and weapon Encyclopedia counts passing their totals.
	Fixed issue where characters with an unknown race would have their body overview tooltip show that they had crotch-boobs, even if they didn't have any.
	Fixed bug where characters' images wouldn't display in their character overview screen if you had the 'American tourist' occupation.
	Fixed issue where you couldn't change your Elemental's surname.
	Fixed bug where attempting to enslave gang members in the Rat Warrens would cause the game to break.
	Fixed issue with pregnancy roulette where sex would end after the character being bred had orgasmed, even if you hadn't orgasmed yet.
	You no longer lose affection with characters in the pregnancy roulette game when sex is automatically ended after orgasming.
	Newly-created characters are no longer considered to have lost their penile virginity if you give them 'handjobs received' experience.
	A character's oral virginity loss description will now correctly be displayed in their body overview screen.
	Fixed issue with Natalya's clothing not being displaced when starting sex with her.
	Fixed issue where sex scenes with pure virgins could sometimes cause the game to lock up and become unresponsive.
	Fixed bug where you could talk to your elemental via the phone action during combat, sex, or other non-neutral scenes.
	Fixed issue where Elementals could use arcane scrolls even though they could not use the upgrade points gained from them.
	Fixed bug where when Lyssieth self-transformed into her human form, her earrings would be unequipped and placed in her inventory.
	Fixed issue with background error being thrown when first entering the Enforcer Warehouse (in Claire's teleportation quest).
	Fixed bug where looking at your item Encyclopedia while trading with an NPC would not show any tooltips and throw numerous background errors.
	Removed ability to contact previous partners in the nightclub if they are no longer attracted to you (if, for example, you've changed your femininity), as it was causing issues with sex immediately ending.
	Fixed issue where maximum limits of testicle size and penis girth were swapped with one another when enchanting clothing with secondary and tertiary size effects.
	Clothing which should be discarded on unequip is no longer placed into the unequipping character's inventory as a result of having body parts transformed (such as unequipping a condom when a character's penis is removed).
	Fixed issue where milking slaves would sometimes not unequip their milking pumps after finishing their work hours in the milking room.
	Fixed issue where opening the 'characters present' screen while managing a slave would result in background errors being thrown and the UI becoming unresponsive.
	Fixed bug where if you ran out of items while enchanting during trading, you'd be able to take all of the shopkeeper's items for free.
	Fixed issue where enslaving your offspring without first beating them in combat would display the interaction interface after enslaving them.
	Fixed issue where slaves generating background sex interaction events would throw background errors if you were in a sex scene at the time they were generated.
	Fixed bug where exiting Dominion locations (such as the City Hall or Enforcer HQ) during an arcane storm would spawn persistent characters on your tile without offering you any interactions with them.
	Upgrading a room into the spa from the Office's 'Occupancy ledger' will no longer place the 'under construction' tile next to the office instead of next to the spa tile.
	Fixed bug where your elemental was being affected by the 'Blinded by Freedom' status effect (from the silly mode's 'American Tourist' background perk).
	Fixed bug where the 'Localised Storm' upgrade for the 'Arcane Cloud' spell would not apply lust damage to the character affected by it.
	Fixed strawberry and blueberry fluid flavour using plural descriptions where all other flavours were singular.
	In her sex scene in Lilaya's room, Rose should no longer have her orifices penetrated during 'quick sex' action generation.

----------------------

DEFAULT KEYBOARD SHORTCUTS:

Format is in:
Primary key | Secondary key (if applicable): Action

You can customise these shortcuts from within the game's options menu.

Esc: Menu
F11: Fullscreen Toggle
W | Up: Move North
A | Left: Move West
S | Down: Move South
D | Right: Move East
SHIFT+W | SHIFT+Up: Response Cursor Up
SHIFT+A | SHIFT+Left: Response Cursor Left
SHIFT+S | SHIFT+Down: Response Cursor Down
SHIFT+D | SHIFT+Right: Response Cursor Right
F5: Quicksave
F9: Quickload
Space | Enter: Select
I | Tab: Inventory
P | J: Phone
M: Map
C: Characters
Z: Zoom
Page Up: Scroll Up
Page Down: Scroll Down
1: Response 1
2: Response 2
3: Response 3
4: Response 4
5: Response 5
SHIFT+1: Response 6
SHIFT+2: Response 7
SHIFT+3: Response 8
SHIFT+4: Response 9
SHIFT+5: Response 10
CTRL+1: Response 11
CTRL+2: Response 12
CTRL+3: Response 13
CTRL+4: Response 14
CTRL+5 | Backspace: Response 15
SHIFT+E: Next Response Tab
SHIFT+Q: Previous Response Tab
E: Next Response Page
Q: Previous Response Page


----------------------

BLOG LINK:

https://lilithsthrone.blogspot.co.uk/

----------------------

"YOU ACTUALLY READ THE README" BONUS!

The debug code is "buggy". Just type that into the game at any point to bring up the debug menu! ^^

Easter eggs:

There is a hand-holding scene with Rose after you gift her a rose (which can be obtained from any of the parks in Dominion).

If you name yourself "James Bond", "Jane Bond", or "Tracy Bond" during character creation, you begin the game with a special weapon.

During 1-on-1 combat with a non-unique character, if you have a penis (and are able to access it), and your opponent has a vagina (and is able to access it), type "dkoma" to instantly defeat and mating press them.

During 1-on-1 combat with a non-unique character, if you have a vagina (and are able to access it), and your opponent has a penis (and is able to access it), type "skoma" to instantly lose and be mating pressed.

In the debug menu's 'Spawn Menu', if you click in the empty space beneath the 'Ranged' button, then you can access the game's hidden cheat items.

----------------------