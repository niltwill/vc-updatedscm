# GTA: Vice City Updated SCM
test:


In short, this mod is supposed to increase the gaming experience with GTA: Vice City. It mostly contains fixes and some improvements.

Besides this, I also recommend to use [NW-Fixes](http://www.mediafire.com/file/ozr53qz061rdc1b/NW_Fixes.zip/file) (and put that one to higher priority in Modloader), the two are quite interrelated now.

**Warning:**
I do not recommend you to use the Save Friendly SCM, at least NOT to overwrite your old save files.
It could corrupt your previous save files, if you use a different SCM for it.
It's best used for a 100% completed save file if you cannot afford the time to restart the game.

Before you load OR overwrite any saved files with the Save Friendly SCM, please create a backup of your save files, so if they get corrupted or anything, you can restore them. The save files can be found under "your username > Documents > GTA Vice City User Files"

The author of this mod does not take any responsibility for damaged or corrupted save files. Use this mod at your own risk and care.


## Installation manual for average user:
<details>
  <summary>Click to expand</summary>
1. Download [Mod Loader](https://github.com/thelink2012/modloader/releases).

2. Also download [ThirteenAG's Ultimate ASI Loader](https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases).

3. First, extract the Ultimate ASI Loader and copy all of its content to where you installed your game (root folder).
This, by default (on 64 bit systems and non-Steam version) should be "C:\Program Files (x86)\Rockstar Games\Grand Theft Auto Vice City"

4. Extract the mod loader archive and
	* copy the "modloader.asi" file to the (now existing) "scripts" folder.
	* copy the "modloader" directory from the archive to the game's installed root folder (as earlier in step 3)

5. Extract "UpdatedSCM" archive and then find and open "Mod Loader Version"

6.Copy "UpdatedSCM" folder to your Mod Loader folder inside of game's root directory

## End of Modloader version installation tutorial.
</details>



##Experienced user installation manual:

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


## Extras

* I highly recommend to check out the few other additional CLEO scripts. See the "readme" file there for more information about what they do.

* If you want to see the "VCPD Cheetah" displayed, then edit "data\default.ide"


	Find line:

	`236, 	vicechee, 	vicechee, 	car, 	CHEETAH, 	CHEETAH, 		null,	ignore, 	10, 	7,	0,		250, 0.7`

	Replace it with (the 6th column with "VCPDCHE"):

	`236, 	vicechee, 	vicechee, 	car, 	CHEETAH, 	VCPDCHE, 		null,	ignore, 	10, 	7,	0,		250, 0.7`


Then edit the appropriate GXT file, and add "VCPDCHE" string with "VCPD Cheetah" or an other localized one. (Note that the included GXT files already contain this change.)


* If you frequently get peds to deliver to at the not-yet-accessible Haitian factory during pizzaboy side mission in Little Havanna, you may overwrite the "paths.ipl". It doesn't do anything else other then removing the ped paths at the Haitian Factory. Afterwards the mission, it's probably the best if you restore the original file.


## Could not fix

* Camera angles when entering/exiting certain interiors (and in some missions) in standard control
* "Can you make SWAT not to attack player after losing the cops when you get out from the bank in The Job..." I tried for a while, but there is not a good outcome, maybe that's why it has been left this way. To get around this problem, I recommend either killing them all or going on a different route. Might try to experiment with this a bit more later on.
* "Make soldiers attack you only when you get into Fort Baxter and make them spawn only in the base" I experimented for a bit, but if the soldiers are friendly to you outside, then civilians seem to spawn inside the base AND no soldiers ever spawn until you get into or near to Fort Baxter. And if you go into the area of the base, then the soldiers will immediately spawn and attack. Therefore, this cannot be tweaked.


## Leftover suggestions

These are not likely to be included any time soon.

* Reimplement a "Get Back in" timer for taxi driver, firefighter and paramedic sidemissions. Not done, due to it being crash prone.
* Implement a trash dash sidemission like in LCS (seems quite complicated).
* "Make taxi driver side-mission more interesting like in GTA VCS that you need to follow the car, rob the shops, and all that in taxi"


## Did not include
* All beta things: UpdatedSCM is NOT a beta mod (despite that it includes some beta stuff). UpdatedSCM aims to keep the vanilla VC experience with a few improvements,fixes and extras but nothing-over-the-line.
