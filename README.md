# GTA: Vice City's Updated SCM

In short, this mod is to increase the gaming experience with GTA: Vice City. It contains mostly fixes and some improvements.


## Backup

ALWAYS make backup before you change any original file.

**Warning:**
I do not recommend you to use the Save Friendly SCM, at least NOT to overwrite your old save files.
It could corrupt your previous save files, if you use a different SCM for it.
It's best used for a 100% completed save file if you cannot afford the time to restart the game.

Before you load OR overwrite any saved files with the Save Friendly SCM, please create a backup of your save files, so if they get corrupted or anything, you can restore them. The save files can be found under "your username > Documents > GTA Vice City User Files"

The author of this mod does not take any responsibility for damaged or corrupted save files. Use this mod at your own risk and care.


## Install with modloader

1. If you don't already have mod loader, download it from GTAGarage:
	http://www.gtagarage.com/mods/show.php?id=25377

2. Also download ThirteenAG's Ultimate ASI Loader:
	https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases

3. First, extract the Ultimate ASI Loader and copy all of its content to where you installed your game (root folder).
This, by default (on 64 bit systems and non-Steam version) should be "C:\Program Files (x86)\Rockstar Games\Grand Theft Auto Vice City"

4. Extract the mod loader archive and
	* copy the "modloader.asi" file to the (now existing) "scripts" folder.
	* copy the "modloader" directory from the archive to the game's installed root folder (as earlier in step 3)

5. Create a new "UpdatedSCM" directory in your "modloader" directory.

6. Copy folders "data", "text" and "to gta3.img" to the newly created "UpdatedSCM" folder.
	-- Alternatively, use one of the other SCM files from the "other_scms" folder. --

7. To be able to enter the interior of the Howlin' Petes, you also need to change a COL file. Extract your "downtows.col" from gta3.img archive and replace the dowbikershop with the one from the "extras" folder. To modify COL files, use steve-m's COL Editor: http://ce2.steve-m.com
	-- This is not required if you use the SCM without MC Tommy.

8. I highly recommend using CLEO: http://cleo.li/download.html
	...and using "extras > cleo > cs-playmodels.cs" + "marina-bay-carpark-wl.cs" one is for the Marina bay carpark water level, and the other is if you wish to have support for all the player CS models. From what I've seen, cleo scripts might not work well under modloader, so copy it to your game root directory's cleo folder instead. And alternatively of using the GXT files, you can use the FXT ones in "extras > cleo > CLEO_TEXT"


## Install manually

If Modloader does not work with Windows XP (or if you do not want to) or your Windows version for some reason, then this is the path to take.

Create a backup of the original files and then do the necessary changes. By default, the root game folder resides in:
	"C:\Program Files (x86)\Rockstar Games\Grand Theft Auto Vice City"

1. Replace "main.scm" with "data > main.scm" file.
2. Replace your preferred language GXT file(s) in the "text" folder. Or alternatively, use CLEO and the required FXT file(s) from "extras > cleo > CLEO_TEXT"
3. Add or replace these new model (and their texture) files to the gta3.img:

	* CSplay12.dff (add)
	* CSplay12.txd (add)
	* CSplay13.dff (add)
	* CSplay13.txd (add)
	* **csruger.dff** (add) <<= make sure to add this!
	* **csruger.txd** (add) <<= make sure to add this!
	* dowbikershop.dff (replace)
	* IGavery.dff (add)
	* IGavery.txd (add)
	* IGdlove.dff (add)
	* IGdlove.txd (add)
	* play13.dff (add)
	* play13.txd (add)

**Warning:**
The game is going to stall in a black screen if you don't add "csruger.dff" and "csruger.txd" in the mission "Supply & Demand", so at the very least, you have to do that! If you don't add IGavery and IGdlove, they will appear untextured (white) ingame. For MC Tommy, please at least use play13.dff and play13.txd. The CSplay12 and CSplay13 is only needed if you use the extra "cs-playmodels" cleo script.




## Extras

* I highly recommend to check out the few other additional CLEO scripts. See the "readme" file there for more information about what they do.

* If you want to see the "VCPD Cheetah" displayed, then edit "data\default.ide"


	Find line:

	`236, 	vicechee, 	vicechee, 	car, 	CHEETAH, 	CHEETAH, 		null,	ignore, 	10, 	7,	0,		250, 0.7`

	Replace it with (the 6th column with "VCPDCHE"):

	`236, 	vicechee, 	vicechee, 	car, 	CHEETAH, 	VCPDCHE, 		null,	ignore, 	10, 	7,	0,		250, 0.7`


Then edit the appropriate GXT file, and add "VCPDCHE" string with "VCPD Cheetah" or an other localized one. (Note that the included GXT files already contain this change.)


* If you frequently get peds to deliver to at the not-yet-accessible Haitian factory during pizzaboy missions in Little Havanna, you may overwrite the "paths.ipl". It does not do more than remove the pedestrian paths at the Haitian Factory. This might or might not prevent the bug that happens with the pizza sidemission at Little Havanna. Afterwards the mission, it's probably the best if you restore the original file.


## Could not fix

* Camera angles when entering/exiting certain interiors (and in some missions) in standard control
* "Can you make SWAT not to attack player after losing the cops when you get out from the bank in The Job..." I tried for a while, but there is not a good outcome, maybe that's why it has been left this way. To get around this problem, I recommend either killing them all or going on a different route. Might try to experiment with this a bit more later on.
* "Make soldiers attack you only when you get into Fort Baxter and make them spawn only in the base" I experimented for a bit, but if the soldiers are friendly to you outside, then civilians seem to spawn inside the base AND no soldiers ever spawn until you get into or near to Fort Baxter. And if you go into the area of the base, then the soldiers will immediately spawn and attack. Therefore, this cannot be tweaked.


## Leftover suggestions

These are not likely to be included, and are just here for reference.

* Reimplement a timer for taxi, firefighter and ambulance sidemissions. Not done, due to it being crash prone.
* Implement a trashmaster sidemission like in LCS (seems quite complicated).
* "Make taxi missions more interesting like in GTA VCS that you need to follow the car, rob the shops, and all that in taxi"


## Did not include

* The teargas: because I don't want to compromise the game stability. You can always use a trainer/CLEO script or edit the SCM yourself. The framerate drop is literally murdering the game, and pretty bad at that (I think it's more than enough to bear with this in The Job mission). Probably way more noticeable if your computer is crap like mine. Sure, it looks cool if you throw it into a crowd and then mow 'em down, but "it takes a long exposure to kill, which is hard to achieve, since people will run like hell from the afflicted area. They won't stop and cough like in SA." All-in-all, the benefits are meager compared to the drawbacks.
* All beta things: UpdatedSCM is NOT a beta VC mod (despite that it includes some beta stuff). UpdatedSCM aims to keep the vanilla VC experience with a few improvements, but nothing-over-the-line. In particular, these phone dialogues have been left out on purpose:

1. BJ Smith's loan shark phone call (after purchasing Sunshine Autos) is not included, because it would make no sense without loan sharks pestering Tommy. This would require a new "debt thread", so that they bother you until you don't pay enough.
2. Some Mercedes phone calls are also not included, because you can't date her and thus, the calls seem out-of-place.
