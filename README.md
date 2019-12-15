![Image description](https://cdn.discordapp.com/attachments/404222921440231435/653619316964458507/updatedscmlogofinal.png)
In short, this mod is supposed to increase the gaming experience with GTA: Vice City. It mostly contains fixes and some improvements.
### Current version: v2.0 new (reorganized)

## Warning:
UpdatedSCM is incompatibile with Stories NPC 'Taxi Service' by Ryadica Cahya (you won't be able to start Paramedic and Firefighter)
I do not recommend you to use the Save Friendly SCM, at least NOT to overwrite your old save files.
It could corrupt your previous save files, if you use a different SCM for it.
It's best used with a 100% completed save file if you cannot afford the time to restart the game.
Before you load OR overwrite any saved files with the Save Friendly SCM, please create a backup of your save files, so if they get corrupted or anything, you can restore them. The save files can be found under "your username > Documents > GTA Vice City User Files"
The author of this mod does not take any responsibility for damaged or corrupted save files. Use this mod at your own risk and care.


## Installation guidelines:

<details>
  <summary>Installation manual for average user: (click me to expand)</summary>
	
1. Download [Mod Loader](https://github.com/thelink2012/modloader/releases).

2. Also download [ThirteenAG's Ultimate ASI Loader](https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases).

3. First, extract the Ultimate ASI Loader and copy all of its content to where you installed your game (root folder).
This, by default (on 64 bit systems and non-Steam version) should be "C:\Program Files (x86)\Rockstar Games\Grand Theft Auto Vice City"

4. Extract the mod loader archive and
	* copy the "modloader.asi" file to the (now existing) "scripts" folder.
	* copy the "modloader" directory from the archive to the game's installed root folder (as earlier in step 3)

5. Extract "UpdatedSCM" archive and then find and open "Mod Loader Version"

6.Copy "UpdatedSCM" folder to your Mod Loader folder inside of game's root directory
</details>



<details>
  <summary>Installation manual for experienced user: (click me to expand)</summary>
	*WARNING: ALWAYS create a backup of the original files and then do the necessary changes.

6. Copy folders "data", "text" to the root game's directory.
	* Alternatively, use SaveFriendlySCM

7. In "data > maps > nbeachw > nbeachw.ide", change line:

`3830, buildingsite2, buildingsite2, 1, 108, 128`

To:

`3830, buildingsite2, buildingsite2, 1, 300, 128`

Change line:

`3948, LODngst2mesh, LODnbeachwbig, 1, 2000, 0`

To:

`3948, LODngst2mesh, buildingsite2, 1, 3000, 132`

Next change the following line:

`3964, bldngst2meshdam, buildingsite2, 1, 135, 132`

To:

`3964, bldngst2meshdam, buildingsite2, 1, 300, 132`

And after that, add this line:

`6308, LODngst2meshdam, buildingsite2, 1, 3000, 132`

(If you didn't mod that file before, you can simply overwrite it with the one included in the package.)

	*Warning: You should use the [Open Limit Adjuster](https://github.com/ThirteenAG/III.VC.SA.LimitAdjuster/releases) to avoid the game crashing after that.

8. To be able to enter the interior of the Howlin' Petes, you also need to change a COL file. Extract your "downtows.col" from gta3.img archive and replace the dowbikershop.col with the one from the "extras" folder. To modify COL files, use [steve-m's COL Editor](http://ce2.steve-m.com).

9. I highly recommend using [CLEO](http://cleo.li/download.html) and using "extras > cleo > cs-playmodels.cs" if you wish to have support for all the player CS models. 
	*Warning: Cleo scripts might not work well under modloader, so copy it to your game root directory's cleo folder instead.

***


1. Replace "main.scm" with "data > main.scm" file.
2. Replace language GXT files in the "text" folder.
3. Add and replace these new models (and their textures) files to the gta3.img:

	* CSplay12.dff (add)
	* CSplay12.txd (add)
	* CSplay13.dff (add)
	* CSplay13.txd (add)
	* **csruger.dff** (add) <<= make sure to add this!
	* **csruger.txd** (add) <<= make sure to add this!
	* **delcsb.dff** (add) <<= make sure to add this!
	* **delcsb.txd** (add) <<= make sure to add this!
	* dowbikershop.dff (replace)
	* IGavery.dff (add)
	* IGavery.txd (add)
	* IGdlove.dff (add)
	* IGdlove.txd (add)
	* **LODngst2mesh.dff** (add) <<= make sure to add this!
	* **LODngst2meshdam.dff** (add) <<= make sure to add this!
	* **nbeachw.col** (replace) <<= make sure to add this!
	* **Downtows.col** (replace) <<= make sure to add this!
	* play13.dff (add)
	* play13.txd (add)

	*Warning: The game is going to stall in a black screen if you don't add "csruger.dff" and "csruger.txd" and also delcsb.dff and delcsb.txd" in the mission "Supply & Demand", so at the very least, you have to do that! If you don't add IGavery and IGdlove, they will appear untextured (white) ingame. For MC Tommy, please at least use play13.dff and play13.txd. The CSplay12 and CSplay13 is only needed if you use the extra "cs-playmodels" cleo script.
	The two LOD model files "LODngst2mesh.dff" and "LODngst2meshdam.dff" also collision file "nbeachw.col" are needed to fix the destroyed construction building, so it remains destroyed from far away as well.

	*Warning: Make sure to replace "nbeachw.col" in gta3.img otherwise the game will crash with an unhandled exception after passing "Demolition Man" and driving away as the LOD model won't be able to find its collisions.
</details>


<details>
  <summary>Extras (click me to expand)</summary>
* I highly recommend to check out the few other additional CLEO scripts. See the "readme" file there for more information about what they do.

* If you want to see the "VCPD Cheetah" displayed, then edit "data\default.ide"


	Find line:

	`236, 	vicechee, 	vicechee, 	car, 	CHEETAH, 	CHEETAH, 		null,	ignore, 	10, 	7,	0,		250, 0.7`

	Replace it with (the 6th column with "VCPDCHE"):

	`236, 	vicechee, 	vicechee, 	car, 	CHEETAH, 	VCPDCHE, 		null,	ignore, 	10, 	7,	0,		250, 0.7`


Then edit the appropriate GXT file, and add "VCPDCHE" string with "VCPD Cheetah" or an other localized one. (Note that the included GXT files already contain this change.)


* If you frequently get peds to deliver to at the not-yet-accessible Haitian factory during pizzaboy side mission in Little Havanna, you may overwrite the "paths.ipl". It doesn't do anything else other then removing the ped paths at the Haitian Factory. Afterwards the mission, it's probably the best if you restore the original file.

I also recommend to use [NW-Fixes](http://www.mediafire.com/file/ozr53qz061rdc1b/NW_Fixes.zip/file) (and put that one to higher priority in Modloader), the two are quite interrelated now.
</details>


<details>
  <summary>To-do: (click me to expand)</summary>

- Fix S.W.A.T attacking the player in "The Job" even through you lost wanted level in Pay'n'Spray.
- Fix Army spawning and attacking the player outside of Fort Baxter.
</details>


## Changelog:

<details>
  <summary>Latest update changelog (click me to expand) (full changelog underneath)</summary>
	
- Replaced Sentinel with Sentinel XS in "The Driver"
- Removed changes related to "slowing down" certain npc's vehicles in missions included in previous releases, we don't want to touch game's difficulty.
- Phil's patriot in "Boomshine Saigon" is now fireproof and Phil will no longer flee out of the vehicle if you'l try to catch the car on fire.
- Ability to skip all of the game help messages when starting new game is back.
- Phone-calls are now skip-able again. (the same way like in GTA SA/LCS)
- Restored the misplaced waitress in "Messing with the man" so you can use a mod to fix her model and animations to see it.
- Moved biker's spawn location in the last cutscene of "Hog Tied" so he'l no longer appear out of nowhere (this is done to support "RestoreCutsceneFOV = 0" option in Widescreen Fix)
- Gang Burrito's are now instantly destroyed once you park Angel in the marker in front of Biker Clubhouse in "Hog Tied" (This is done to prevent some weird stuff going on on the cutscene like in the original)
- Removed script-related censorship for German and French languages.
- Fixed misplaced release switch sphere in "The Fastest Boat"
- -Fixed sphere in front of the panel not being removed on the cutscene when Tommy presses release switch in "The Fastest Boat"
</details>

<details>
  <summary>Full changelog (click me to expand)</summary>
Fixes:

- The Ocean View Hotel's lightning issue fixed (the door was very black and the interior was darker than what it's supposed to be). 
- Fixed the sphere in front of the Ocean View Hotel during the intro, now it's destroyed as soon as you approach the marker instead of after the cutscene ends.
- Fixed some grammar mistakes regarding death messages of NPCs in the missions (LCS/VCS uses the same approach)
- You no longer have to be in a vehicle after loosing wanted levelin 'Treacherous Swine' for the mission to pass. (now you can indeed pass it on foot or in a vehicle, you don't have to use the Pay 'n' Spray)
- Vehicles in 'The Party' will no longer despawn and spawn again after the yacht cutscene, resulting in the player's vehicle and the parked cars getting repaired if you damaged them before the cutscene.
- Fixed a bug where severe side-missions wouldn't play "Mission Passed" sound after you pass them.
- You can no longer go back with the boat in 'The Fastest Boat' before releasing it from the docks.
- The courier should no longer get stuck if you skip his cutscene in 'Mall Shootout'
- Fixed the appearance of the construction building that you destroy in 'Demolition Man'
- The third Cuban should also die now if he somewhat gets stuck while charging at the sniper in "Cannon Fodder"
- Fixed looped arrow marker in the mission "V.I.P" (that's the reason behind why it seemed standstill) and delivering client with the rival taxi will no longer fail the mission.
- Game no longer crashes when you type cheat BIGBANG to destroy all vehicles in first cutscene while Ken is driving to his office (making this a fast way to get your game started if you're impatient)
- Weather will now reset to extra sunny (like the other two Avery missions) in Two Bit Hit (previously if it's raining, the rain falls inside the limo)
- "Use this" subtitle will now be displayed in 'Treacherous Swine' at the right timing.
- Fixed(?) random traffic vehicle passing by in 'Alloy Wheels of Steel' (might be sometimes visible)???
- In 'Sir, Yes Sir' mission, "I'm getting out of here" will no longer play if both the soldiers in the tank are dead, and the "Civilian in the TANK! STOP HIM!" will no longer play if all soldiers are killed?????
- GDA now spawns earlier, before Phil says "I told you not to touch that alarm!" (before you can see him spawning if you quickly jump down from upstairs)
- Fixed randomization in FUD.
- Game no longer says 'tutorial' messages around Ocean View Hotel while on a mission?????
- Fixed the text bug with 80 hidden packages (now will say either Diaz's Mansion or Vercetti Estate)
- Male ped in 'The Shootist' is now the one used in the cutscene instead of MALE01.
- Fixed some male actors being created as female ones.
- Prostitute health bonus is no longer removed upon saving.
- Fixed widescreen issues in Avery missions and at the end of G-spotlight.
- The player can no longer move before the cutscenes in Avery missions (previously you could even move enough to KO yourself with the limo)
- Fixed the model destroys at the end of 'Jury Fury'???
- The GiGN no longer disappear after you chase after Pierre in the mission 'Mall Shootout'???
- Fixed bug in 'The Shootist' when you start mission using a weapon that's not a Colt pistol???
- Fixed the stuck animation in 'The Fastest Boat' after releasing the Squalo.
- In 'Treacherous Swine', after you start the mission (finished initial cutscene) in the black fade you can no longer move (previously you can accidentally get into the water)
- Fixed cutscene's end when buying the Cherry Popper Icecreams asset (previously the old lady remains visible)
- Fixed dark sky glitch in severe missions: 
	- after cutscene in 'The Fastest Boat'
	- during "Skakedown"
	- during "Bar Brawl"
- The weapons for sale at Ammu-Nation / tool stores were wonky or floating out of bounds: now the weapons lie flat against the wall instead of floating away from it.
- Fixed the Pole Position Strip Club's dark world bike glitch. (!!!Need to check if this fix is still there as you updated interior.txt with possibly older older one)
- Lot of GXT (text) fixes and improvements.
- In 'Hog Tied', Tommy no longer gets stuck when leaving the bike at the mission's end.
- Fixed the cellphone-weapon selecting glitch (prevents Tommy from glitching weapons in place of phone during a call and its the same exact behaviour like in LCS) 
- Several various bugfixes in sh*t (structure errors, but now also shuffles between ALL random dialogues)
- Fixed some broken vehicle spawn points these being:
	- The rewarded Hunter at Ocean Beach is now positioned at the helipad properly.
	- Now both the Admiral and Stretch spawns simultaneously at the Mansion.
- Fixed the bodyguards in Vercetti Estate almost never spawning (the ones you get after 100% completion)
- Fixed the quadruple insane stunt.
- Fixed mansion spawn point for Pizzaboy, after completing the Pizza Delivery sidemission, it now spawns properly (only after you passed the mission 'Rub Out').
- The hidden package under Starfish Island bridge is no longer below the ground.
- Fixed Havana Outfit (cuban) clothing pickup being no longer accessible if you do some missions in certain order.
- Fixed a player animation stuck bug in 'The Job' (when you get out of the car around the bank area).

- Some fixes from the Japanese re-release:
	- The message 'Come back when you have finished the Biker gang missions.' is shown for 4 seconds instead of 1
	- Duration of Pole Position mission complete cutscene is slightly longer.
	- The Infernus spawn inside the mall is disabled during 'All Hands On Deck!'
	- The driver of Candy's car in 'Recruitment Drive' can no longer be shot while in the car.
	- The limo driver and Candy can no longer be shot while in the car in 'Martha's Mug Shot'. In addition, the driver no longer 		responds to threats and the limo is fireproof.
	- During 'Cannon Fodder', the player now leaves the taxi slightly before the Cubans, instead of right after.
	- The Voodoo's with Cubans in 'Trojan Voodoo' are now fireproof, and the Cubans no longer respond to threats.
	- The Topfun van is no longer locked in position at the end of 'Bombs Away!'
	- Bugfix in 'Love Juice' regarding trying to pick up Mercedes. It is now only possible in a car or motorcycle (with exception 		Pizza Boy/Baggage) as per instructed. No more easy heli rides!
	- The player is now removed from any vehicle and the vehicle despawned after the intro cutscene in 'Publicity Tour' if he was 		in one.
	- Lance now appears as IGBudy3 instead of the usual IGBuddy in 'Death Row'.	


Changes and improvements made to the original:

- The "press TAB to answer the call" textbox should now always display, the game now correctly destroys previous textboxes????
- Added 'Time' indicator next to the clock in Vigilante, Firefighter, Paramedic, Pizzaboy, Shooting Range and Cone Crazy missions, like it appears in other GTA games
- The Love Fist limo now has a 10% chance of alarm going off once you steal it
- Added a briefcase in restored 'Supply & Demand' cutscene.
- Removed Tommy hand animations in 'Treacherous Swine' when shouting at Gonzalez because of holding a chainsaw which is heavy.
- Added a 'TIME:' next to the timer in the 'PCJ Playground' like in other side missions and GTA VCS.
- Silent's contribution: 'The Job' mission code cleanup)
- Patients in the Paramedic side-mission will now only enter the Ambulance when it is stopped (preventing from easy accident killings)
- The Pole Position Club is now accessible without buying it, and the private service is also available, but it will cost you $50 each segment instead of $5 and it will not complete the asset mission, regardless of how much you stay, without you buying the asset first
- Text colorization is mostly restored to the default pink ones (in american.gxt and american.fxt)????
- Included the spanish translation now
- Vercetti's Gang car changed to Banshee from Stallion
- In 'Jury Fury', damaging the Admiral will now make the jury enter the car instead of just doing nothing
- Cubans entering your vehicle at the start of 'Cannon Fodder' now takes longer than two seconds

- Rico should now fade away at end of 'Cannon Fodder' (and also unkillable by the player during that time, since he is vital to the upcoming storyline)???
- Timer in taxi mission will be set according to destination each time, thus the time will not increase infinitely anymore??????
- You cannot start the mission 'Alloy Wheels of Steel' if in the cop outfit.
- No more infinite ammo with the pistol in 'The Shootist' in the first round, and you can also no longer shoot before the message "live ammunition...
- Time is now adjusted to 23:00 when you visit Cortez's yacht in 'The Party' (due to the Colonel saying: "Buenas noches!" - indicating night time)??
- The target in 'Four Iron' will now escape when you hit him with a (not-so-deadly) weapon from the distance (otherwise if you do not get too close, you can easily kill him without him moving an inch)
- In 'All Hands On Deck', the heli drivers and hunter driver are changed to FSFA
- Lance will now say "Come on man, drive more careful!" if you damage the Infernus quite some in 'Back Alley Brawl'. (The other with the Strip Club is removed, as it conflicts with the other, there can only be one dialogue and because we first have to buy that before we can even enter it, so it makes no sense for Lance to say that! Not to mention we got sorta introduced to it in the first mission.)?????
- You can now skip tutorial messages and info pickups at the start of the game. Press the SPRINT button to quit the player lock and go on without having to wait a little, or press the ACTION key under 6 seconds to remove help. If no action is taken, game includes help after 6 seconds. This does not have much impact on the game, it's merely an additional option for the seasoned players who don't need this info being repeated.
	In no-help mode, some of these missions' help messages are also disabled:
		- The Party (follow the T-shirt blip)
		- Back Alley Brawl (attacking and sprinting help)
		- Jury Fury (weapon cycling help, hardware store hint)
		- Riot (cycling through targets, weapon drop help, explosive barrel help)
		- Four Iron (the golf club help when you enter a Caddy)
		- Demolition Man (the control of the RC heli)
		- Mall Shootout (ammu-nation hint, triangle blip help)
		- Guardian Angels (the assault rifle help, crouching, bike drive-by help)

- Phil now sits in the left side of the Patriot in Boomshine Saigon??????
- In 'Sir, Yes Sir!' mission, the army now use M4 instead of Ruger
- In 'The Job' mission, you will now have to lose your wanted level before initiating the bank robbery
- Increased bike's health in 'G-spotlight'
- The taxi driver in taxi sidemission will not enter as passenger anymore (because when he does, Tommy can no longer enter back to that taxi)??????
- Added slow motion effect in 'Psycho Killer' while the psycho kills the security guard (in one shot now)??????
- No more afternoon time setting in 'Supply & Demand'
- Skimmer inside large hangar at airport now spawns after mission 'Dildo Dodo'????
- Romero Hearse now spawns next to the pizza restaurant in Little Haiti after 'Two Bit Hit'
- Changed text from "Mission failed" to "Pizza mission ended" when you turn off pizza mission needs revisit the text??
- Fixed camera in 'The Party' after leaving Rafael's (now facing towards the bike)?????
- Player is no longer facing towards the Lawyer's office in 'Jury Fury' after the opening cutscene????
- In 'Riot', after getting the worker clothes you will no longer face Rafael's entrance???
- The 'G-spotlight' mission now starts at 22:00 instead of 17:00
- Added two star wanted level if you fail the mission 'Waste the Wife'
- Changed the two identical HMYAP peds in the Bobcat in 'Autocide' (now the driver is BMODK)
- Vehicles and targets no longer instantly disappear in 'Autocide'
- Replaced the HMYRI ped in 'Road Kill' with the Burger guy
- Army gang now carries MP5 as secondary weapon???
- Vercetti's gang now uses the Stallion.
- Moved the unique white admiral at the mansion and tucked it next to the stairs
- Random possibility of vigilante and ambulance vehicles being either locked.
- Lowered percentage of alarm triggering on Admiral at Vercetti's mansion (25% instead of 50%)
- Added a second Securicar at the bank
- In 'Jury Fury', the woman the jury is talking to will now disappear (with running) instead of remaining in the alley motionlessly
- Limos now have unique colors in 'Keep Your Friends Close'
- The mobs now wear Uzi instead of Tec-9s in 'Keep Your Friends Close'?????
- Sonny's ruger is replaced to M4 in 'Keep Your Friends Close'?????
- After you release the Squalo in 'The Fastest Boat', an alarm will sound off
- The Diaz goons in 'Treacherous Swine' are now CLA and CLB (originally they are both CLA)
- The shark goons no longer fly the sparrows during "Phnom Penh '86" (HMORI -> sea sparrow, WMOBU -> sparrow)???
- Moved the golf outfit pickup from the Golf Club entrance back to 'Jocksports' store in Vice Point
- Moved Candy closer to the limo in "Martha's Mug Shot", also changed one GDA to GDB (if you use a different texture for him)needs tweaking
- In 'Psycho Killer', added HMYAP ped to drive the Trashmaster, also changed one GDA to GDB (if you use a different texture for him)
- In 'Naval Engagement', fixed Rico standing far too close to the edge of the pier, also edited checkpoint to reflect this???
- Restored unused snoring sound effect in 'No Escape?' and changed the seated cop's animation to Lance's as seen on 'Death Row' (the animation will reset after you break Cam out)????
- In mission 'Cop Land', added alarm to the coffee shop once you blow it all to hell, also reduced the fade a little in an attempt to hide the transition
- In mission 'RC Bandit Race', randomized the vehicle colours (originally all were always the same colour)
- The PSG-1 (laser) rifle pickup is changed to the regular Sniper one in 'Cannon Fodder'
- In 'All Hands On Deck!' mission, the GiGN now arrive in the FBI Washington (instead of the regular Washington)needs to be removed makes no sense
- More bad guy variety in 'The Fastest Boat' (looks better than having to face the same HMYST guys)
- In 'Demolition Man', now HMYAP and WMYCW are the workers (instead of just WMYCW)
- In 'Demolition Man', there is now GDA and GDB instead of just GDA (if you use a different texture)
- In 'Treacherous Swine', at the penthouse, if you park a vehicle near the entrance it will now disappear when Gonzales is leaving???
- Added a chauffeur, Avery Carrington and Donald Love when the limo arrives
- From the Coach controlled by the AI, random peds will exit now and not only MALE01?????
- In 'All Hands on Deck!', Colonel's sailors have more difference in models (instead of all being CGONA)
- After 'All Hands on Deck' and 'Rub Out' mission is completed, the speeder you earned will spawn at Vercetti's mansion????
- Increased Diaz's health in 'Rub Out' to increase difficulty?????
- Increased Sonny's and Lance's health in 'Keep Your Friends Close' to increase difficulty??????
- In 'Supply & Demand', CBA and CBB is used instead of just CBA
- In 'Supply & Demand', the freelancer is now visible on the Marquis
- In 'Supply & Demand', Lance is now visible in the Squalo before you trigger the cutscene
- Added unused cutscene in 'Supply & Demand'
- 'Supply & Demand' now takes place during daytime because of the seagull sound in the readded cutscene
- Increased garage vehicle storage limit, small garages now can hold up to 2 vehicles (like a car and a bike) while all other garages up to 4 vehicles???
	- Links View Apartment: 2
	- Ocean Heights Apartment: 2
	- El Swanko Casa: 2
- Health pickup in front of Ocean View hospital moved to the entrance doors (this fix needs revision to match vcs position)
- Bank job mission(s) will now only be available after you finish with Kent Paul's phone call
- BMYBB and WMYST model used in 'Recruitment Drive' instead of three BMYCR
- Different models now used for enemies in 'Gun Runner' (BMYCR, BMYPI, HMYRI, HMYST, WMYCR)
- Spaz shotgun replaced to Stubby shotgun and M60 to M4 in 'Gun Runner' (smaller weapons more fitting to the small crates)
- The counter for drug deals (Distribution) no longer resets back to 0 (only after 1000 deals), it keeps adding up (no longer need to do 50 all at once)
- Slightly increased detection of the pizzabox because sometimes when you toss the pizza at them, they don't comprehend it
- Red Tracksuit outfit now gets unlocked after completion of Juju Scramble (instead of being available since the very beginning of the game)
- Increased the owners health in Ammu-Nation and tool stores (they do not die as quickly now)
- Moved Phil to back seat of Patriot in 'Boomshine Saigon'
- Rico's boat is now removed after completing 'Stunt Boat Challenge'
- Restored Lance's beta lines in 'Back Alley Brawl' (only plays when you go near the Pole Position Strip Club)????????
- In 'Autocide' when you quickly kill both Marcus Hammond and Franco Carter, game will no longer say they have noticed you?
- In 'Cop Land' ending at the "asset text" display, the camera is moved to hide the 'see-through' entrance????
- Added more ped variety in 'The Job' (inside the bank)
- Tommy is relocated at the back seat of the Admiral in intro cutscene.
- Post mission monologues in KENT1 and BARON5 are now handled by a separate script
- All R3 submissions now require a double-tap to cancel, like in LCS and VCS
- Fixed all-caps ragetext in Navel Engagement mission - KILL ALL THE HAITIANS ON THE BOAT -> Kill the Haitians on the boats
- Tidied up dialogue from 'In the Beginning' (Subtitles now synchronise properly)????
- 'Ocean View' --> 'Ocean View Hotel'????
- PCJ 600 --> PCJ-600?????
- Criminal rating status 'Leece' --> 'Leech'????
- Tidied up the 'Publicity Tour' dialogue????
- Renamed some of the places on the Map Legend???
- Renamed 'Kruger' from 'Guardian Angels' back to PS2 'Ruger'??
- Corrected some of the places on the Map Legend????
- Updated save prompt text, coloured the pickup text name, and re-added missing text indicating that saving the game advances the time by six hours???
- Tidied up the phonecall dialogue (Sonny's first call, Lance etc.)
- Escobar International --> Escobar International Airport
- BLOODRA --> Bloodring Banger (Oceanic)
- BLOODRB --> Bloodring Banger (Glendale)
- Updated the 100% complete message
- 'You have been awarded the fast reload skill' --> 'You have unlocked the fast reload ability!'
- Updated 'Martha's Mug Shot' mission text (originally using PC hotel name) also fixed up previously unnoticed grammar mistakes
- 'Havana' clothes --> 'Cuban'
- Updated pickup names for tracksuits (now you can tell which colour is which, and which is unlocked on what mission; I.E - Black tracksuit outfit delivered to downtown etc)
- VCS styled the clothing names --> 'Casuals'?????
- 'New clothes' --> 'Frankie' outfit????
- Highlighted mission specific clothing you unlock after each mission????
- Expanded 'street' outfit text - Added info about changing and altering player skin from options (partly taken from PC manual)???
- 'Bank Job' --> 'Bank Robber'
- Fixed all-caps raegtext in credits, everything's properly capitalized / fixed?????
- Styled the taxi destinations like VCS, renamed literally everything. Hospitals now named to what it says in the manual?????
- Fixed up the paramedic text???????
- Fixed the wrongly coloured text in 'Autocide'?????
- Added bit of dialogue where Tommy says 'I work for-' before Diaz tells him to shurrup?????
- Fixed up the ice cream factory dialogue?????
- Tidied up cutscene / mission dialogue for 'The Party'?????
- Tidied 'Back Alley Brawl' dialogue / mission text????
 - added missing coloured text to match destination blips????
 - more colored text where it should be???
- Tidied 'Jury Fury' dialogue / mission text
 - added missing coloured text to match destination blips
- Completed the entire credits list???
- Hotring racers now have these names:?????
 - 'HOTRINA' --> 'Hotring Sunbeam'
 - 'HOTRINB' --> 'Hotring Thunderbird'
 - 'HOTRING' --> 'Hotring Lumia'
- Fixed up Auntie poulet's mission dialogue?????
- Improved the outfit delivered text even more????
- Coloured some of the mission text for 'Jury Fury' 'Demolition Man' 'The Party'
- Corrected the raeg text given for unique jumps???
- Fixed the wrongly positioned text for 'walk through the doors of the Ocean View Hotel'
- Coloured more of the mission specific dialogue where it was needed
- Corrected raeg caps for wheelies / stoppies????
- Fixed up the hidden package reward names so they're coloured like the outfit delivery messages????
- Cheetah, Infernus, Stretch and Banshee no longer disappears in "The Party".???????
- GDA and GDB appear as the security now (so one can give a different texture to GDB)
- In 'Hog Tied' mission, the shark gang members no longer fade away like ghosts.
- Added MC Tommy outfit (available after completing 'Hog Tied' mission).
- Drug dealer in Love Juice changed to BMYCR from BMYBB????
- You can no longer block the courier's path with a car in "Mall Shootout" (at the exit).
- Mesa Grande in Fort Baxter Air Base (like on VCS, spawns after mission "The Fastest Boat") revisit pls logic
- Stretch in front of hotel in Washington Beach near the Pay 'n' Spray by Apartment 3C
- Fixed monologues after KENT1, after Avery's business advice call
- Fixed monologue in BARON5 - now plays only after the mission is passed
- Fixed monologues in ROCKB1, COUNT1, CAP_1 - their behaviour now matches stock post-cutscene monologues
- Removed unused code from OVALRNG, JUNKFUD, HJ, USJ, sh*t, SECURI, IMPORT, CELL, PICKUPS
	- Note: Save-friendly SCM doesn't seem to load old save games with these above, so it remained as it was.
- Mercedes will now only say "Do you mind me resting my hand in your lap?" in 'The Party' mission if she sits next to you in a car.
- Added two extra audio lines in "The Job" by Tommy if you get the attention of the cops: "Crap, now the cops are onto us!", "And we're not even there yet!"
- Fixed the borked vehicle spawn points and added Zera's fixed vehicle spawn points (and forgot to mention some of these).
 	- Phil's Patriot position slightly changed.?????
- Tommy's clothes are no longer reverted to his default one when entering missions 'Riot', 'Four Iron', 'No Escape?', 'Cop Land'.
- Voodoo model now gets destroyed in 'Cannon Fodder' instead of the non-existing 'Stinger' (original car)????
- Hotring cars now spawn as a reward after completing the mission "Hotring" (similarly to Bloodring)??
- Spand Express now spawns regularly after you complete "Riot" (at that mission location)
- The "An Old Friend..." as the latest mission if you save the game before Lawyer's first mission is now displayed instead of "In the beginning..."????
- Added the PS2 scene skips in the intro "Enter does a full skip and Shift/Space/LMB do partial skips. Also made the gamepad do a full skip with Cross/A and partial skip with Triangle/Y. Both Cross and Start just perform a full cutscene skip."
- In mission 'Jury Fury', the woman the jury talks with is WFYBU instead of BFYBE, and the golfer now runs over a construction worker (WMYCW) instead of dockworker (HMYAP)
- After the Spand Express van hits the Admiral in 'Jury Fury', it now drops a screwdriver and a hammer, instead of two hammers.
- Speeder given by Cortez now matches colour of the one attached to the yacht.
- Ingame maverick from "Phnom Penh '86" now matches the cutscene Maverick's colour
- Tommy's sitting position inside the Maverick is now at the back seat in mission "Phnom Penh '86" (when picked up by Lance after you got the money) that doesn't make any sense
- Tommy now walks over to Lance's Stallion during the beginning of 'Rub Out'.
- Random stinger blocking Haitian Drug Factory Entrance during 'Cannon Fodder' replaced with a Voodoo
- Restored unused 'yt_gangplnk_tmp' prop at the marina
- Added long-needed Ambulance spawn point in front of hospital in Little Havana (similar to Vice City Stories).
- Solid black palette used for UC vehicles changed to a lighter shade (still black).
- At the Pole Position Strip Club, if the barkeeper's alive, she will now say some random lines to you if you get nearby to the counter (these were unused audio).
- Restored Tommy's speaking animation with the french in "Mall Shoutout" and with Lance in "Guardian Angels" (at the carpark).
- Lance now doesn't disappear instantly in Guardian Angels after the bike ambush (if you ever looked back before getting on the bike, he just vanished without a trace...).
- Phnom Penh '86 now includes three additional audio lines: "You sure is better at shooting than talking." and "Thanks. You're a real charmer yourself." and "I know, Tommy."
- Supply & Demand now includes the lines: "We made it! Those other boats ain't VIP class." (when reaching the Marquis), "They're matchwood! And fish food!" while damaging the cuban ships, plus "Bridge coming up!" after the jetty part (if the helicopter is still there).
- In The Job mission, Tommy now says "New threads, huh? You need more than that, pal!" during the closing cutscene in response to Kent Paul. Also the line from "Yeah, and you'll put somebody's eye out!" is now said after "For god's sake, Phil, stop waving that thing around!"
- Removed a misplaced pedestrian in the cutscene of the mission 'Messing With the Man' (only his head was visible).
- Added some audio lines ingame:
	- During the mission "The Chase" after the Shark boss gets into the BF injection, Tommy will soon make the remark: "Sick of 		these pricks!"
	- During the mission "Death Row", Diaz's goons will taunt you verbally at the junk yard: "Do you think you can get away with 		this?".
	- During the mission "Keep your Friends Close", Tommy will now shout "Sonny? SONNY! I'm coming for ya!" in response to Sonny's 		killing order.
	- Strippers now say some comments to you in the Pole Position Club when the camera changes, at the private stripteaser room. -		This might increase the monotonous scene's atmosphere a bit.

- Phone call additions:
	- During Umberto Robina's call, Tommy will now reply with an additional "Yeah, maybe..." when Umberto asks: "wanna work for 		me?"
	- Ken Rosenberg now gives you some business advice (after completing the mission 'Shakedown')
	- Kent Paul rings you up regarding the the SWAT retirement fund which is later seized in the mission 'The Job', happens shortly 		after you purchase the Malibu Club.
	- Phil Cassidy now calls after you complete the last storyline mission (Keep your Friends Close)
	- Mercedes now also rings you up after you complete the mission 'Rub Out'.
	- Mercedes now rants to you about Jezz Torrent after you complete the mission 'Love Juice'.

- Tommy is more talkative and says a few more inner-monologues to the player:
	- After completing the mission 'Death Row'
	- After completing the mission 'Rub Out'
	- After initial cutscene of 'Love Juice'
	- After initial cutscene of 'Spilling the Beans'
	- After initial cutscene of 'Cap the Collector'
	- After finishing with Avery's business advice call (after 'Shakedown')
</details>


<details>
  <summary>Save-friendly changelog (click me to expand)</summary>
This save-friendly version contains only fixes, but nothing that would make your old save game files crash or force you to start a new game.
Audio additions are all removed because they might cause some ... bugs and then make it unable to complete the game..The old saved ones.
Also there are no model changes of any kind. Though some vehicle additions exist as CLEO scripts.

! Warning !
Despite these changes not breaking old save games, in these saved games you _might_ see weird glitches like an unusual floating building,
something misbehaving, or some missing collision. So use this at your own risk and it's still best practice to start a new game above all else to make sure everything goes smoothly!


[*] Removed a misplaced pedestrian in the cutscene of the mission 'Messing With the Man' (only his head was visible).
[*] Speeder given by Cortez now matches colour of the one attached to the yacht.
[*] Ingame maverick from "Phnom Penh '86" now matches the cutscene Maverick's colour
[*] Tommy's sitting position inside the Maverick is now at the back seat in mission "Phnom Penh '86" (when picked up by Lance after you got the money)
[*] Restored Tommy's speaking animation with the french in "Mall Shoutout" and with Lance in "Guardian Angels" (at the carpark).
[*] Lance now does not disappear instantly in Guardian Angels after the bike ambush (if you ever looked back before getting on the bike, he just vanished without a trace...).
[*] Fixed a player animation stuck bug in 'The Job' (when you get out of the car around the bank area).
[*] Tommy now walks over to Lance's Stallion during the beginning of 'Rub Out'.
[*] The hidden package under Starfish Island is no longer below the ground.
[*] Player can move around after picking up the chef's cellphone, instead of being locked in place.
[*] Solid black palette used for UC vehicles changed to a lighter shade (still black).
[*] Tommy's clothes are no longer reverted to his default one when entering missions 'Riot', 'Four Iron', 'No Escape?', 'Cop Land'.
[*] You can no longer block the courier's path with a car in "Mall Shootout" (at the exit).
[*] In 'Hog Tied' mission, the shark gang members no longer fade away like ghosts.
[*] In 'Hog Tied', Tommy no longer gets stuck when leaving the bike at the mission's end.
[*] Cheetah, Infernus, Stretch and Banshee no longer disappears in "The Party".
[*] Added two star wanted level if you fail the mission 'Waste the wife'
[*] The GiGN no longer disappear after you chase after Pierre in the mission 'Mall Shootout'
[*] The 'G-spotlight' mission now starts at 22:00 instead of 17:00
[*] Fixed widescreen error at the end of G-spotlight
[*] Decreased the speed of Hilary's Sabre Turbo a bit
[*] Moved Candy closer to the limo in "Martha's Mug Shot"
[*] In mission 'RC Bandit Race', randomized the vehicle colours (originally all were always the same colour)
[*] Decreased the last target's bike speed in 'Autocide'
[*] Vehicles and targets no longer instantly disappear in 'Autocide'
[*] In 'Naval Engagement', fixed Rico standing far too close to the edge of the pier, also edited checkpoint to reflect this
[*] In mission 'Cop Land', added alarm to the coffee shop once you blow it all to hell, also reduced the fade a little in an attempt to hide the transition
[*] In 'Jury Fury', the woman the jury is talking to will now disappear (with running) instead of remaining in the alley motionlessly
[*] The speed of drug dealer in 'Love Juice' is slightly decreased
[*] In 'Treacherous Swine', after you start the mission (finished initial cutscene) in the black fade you can no longer move (previously you can accidently get into the water)
[*] In 'Treacherous Swine', at the penthouse, if you park a vehicle near the entrance it will now disappear when Gonzales is leaving
[*] After you release the Squalo in 'The Fastest Boat', an alarm will sound off
[*] Fixed the stuck animation in 'The Fastest Boat' after releasing the Squalo
[*] Fixed widescreen errors in Avery missions
[*] The player can no longer move before the cutscenes in Avery missions (previously you could even move enough to KO yourself with the limo)
[*] Limos now have unique colors in 'Keep Your Friends Close'
[*] Fixed dark sky glitch after cutscene in 'The Fastest Boat'
[*] Fixed cutscene's end when buying the Cherry Popper Icecreams asset (previously the old lady remains visible)
[*] Lance is no longer visible when you go back after you got the briefcase in 'Guardian Angels'
[*] Slightly increased detection of the pizzabox because sometimes when you toss the pizza at them, they don't comprehend it
[*] Moved Phil to back seat of Patriot in 'Boomshine Saigon'
[*] Rico's boat is now removed after completing 'Stunt Boat Challenge'
[*] In 'Autocide' when you quickly kill both Marcus Hammond and Franco Carter, game will no longer say they have noticed you
[*] In 'Cop Land' ending at the "asset text" display, the camera is moved to hide the 'see-through' entrance
[*] Tommy is relocated at the back seat of the Admiral in intro cutscene
[*] Fix some male actors being created as female ones
[*] You now need to get into a car to pass the mission in 'Treacherous Swine'
[*] Added slow motion effect in 'Psycho Killer' while the psycho kills the security guard (in one shot now)
[*] Increased bike's health in 'G-spotlight'
[*] GDA now spawns earlier, before Phil says "I told you not to touch that alarm!" (before you can see him spawning if you quickly jump down from upstairs)
[*] Phil now sits in the left side of the Patriot in Boomshine Saigon
[*] In 'Sir, Yes Sir!' mission, the army now use M4 instead of Ruger
[*] Time is now adjusted to 23:00 when you visit Cortez's yacht in 'The Party' (due to the Colonel saying: "Buenas noches!" - indicating night time)
[*] The target in 'Four Iron' will now escape when you hit him with a (not-so-deadly) weapon from the distance (otherwise if you do not get too close, you can easily kill him without him moving an inch)
[*] No more infinite ammo with the pistol in 'The Shootist' in the first round, and you can also no longer shoot before the message "live ammunition..."
[*] "Use this" subtitle will now be displayed in 'Treacherous Swine' at the right timing
[*] Weather will now reset to extra sunny (like the other two Avery missions) in Two Bit Hit (previously if it's raining, the rain falls inside the limo)
[*] Game no longer crashes when you type cheat BIGBANG to destroy all vehicles in first cutscene while Ken is driving to his office (making this a fast way to get your game started if you're impatient)
[*] In 'Jury Fury', damaging the Admiral will now make the jury enter the car instead of just doing nothing
[*] The bike in 'G-Spotlight' is now damage-proof
[*] Cubans entering your vehicle at the start of 'Cannon Fodder' now takes longer than two seconds
[*] The third Cuban should also die now if he somewhat gets stuck while charging at the sniper
[*] Rico should now fade away at end of 'Cannon Fodder' (and also unkillable by the player during that time, since he is vital to the upcoming storyline)
[*] In 'V.I.P.', fixed looped arrow marker (that's the reason behind why it seemed standstill) and delivering him with the rival taxi will no longer fail the mission
[*] Patients in the Paramedic side-mission will now only enter the Ambulance when it is stopped (preventing from easy accident killings)
[*] The courier should no longer get stuck if you skip his cutscene in 'Mall Shootout'
[*] You can no longer go back with the boat in 'The Fastest Boat' before releasing it from the docks
[*] Tweaked the wanted level check in 'Treacherous Swine' (now you can indeed pass it on foot or in a vehicle, you don't have to use the Pay 'n' Spray)
[*] Removed Tommy hand animations in 'Treacherous Swine' when shouting at Gonzalez because of holding a chainsaw which is heavy.
[*] Fixed a bug where "Mission Passed" sound wouldn't play after 'PCJ Playground' is passed (Rockstar's Bug)
[*] Added a 'TIME:' next to the timer in the 'PCJ Playground' like in other side missions and GTA VCS.
[*] Fine-tuned the car health's check in 'Jury Fury' (hitting it with the fist once or very slightly damaging the car would not not trigger the nearby jury's attention before)
[*] PCJ-600 in 'G-spotlight' now has increased health so it won't be possible to catch fire with it easily (previous fix didn't work as for some reason the game ignores damage-proof code on bikes)
[*] Added 'Time' indicator next to the clock in Vigilante, Firefighter, Paramedic, Pizzaboy, Shooting Range and Cone Crazy missions, like it appears in other GTA games
[*] Vehicles in 'The Party' will no longer despawn and spawn again after the yacht cutscene, resulting in the player's vehicle and the parked cars getting repaired if you damaged them before the cutscene
</details>

## Special thanks to:
 - Noskillx (Organization & coding)
 - Silent (Organization & coding)
 - Kalvin (MC-Tommy outfit)
 - B_Smiles (quadruple insane stunt as well as vehicle spawn fixes)
 - Blackbird88 (Havava outfit fix)
 - Matt1010 Realization of the logo.
