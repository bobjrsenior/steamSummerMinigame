# Steam Summer 2015 Monster Minigame AutoScript #

## Purpose ##

it cheats for you.

This fork has:
* Elemental damage prioritizing, gold prioritizing
* Auto clicking
* Tickrate set to 1000ms every second
* Disable most particles
* Auto use abilities
* idk


## Features ##

- Moves you to the lane most likely to give you gold, prioritized like so:
	1. The lane with a Treasure Minion or Boss
	2. The lane with the Miniboss with the lowest health
	3. The lane with a Spawner below 40% health
	4. The lane with a Creep below 10% health
	5. The lane with the Spawner with the lowest health
- Activates most reusable abilities, if they are purchased and cooled down:
	- Medics if your health is below 50%
	- Morale Booster, Napalm, and Cluster Bombs if the lane has a Spawner and 2-3 Creeps
	- Good Luck Charm as soon as possible
	- Tactical Nuke if the current Spawner is between 60% and 30% health
- Activates some items if you have them and the situation calls for them:
	- God Mode if Medics is in cooldown and your health is low
	- Cripple Spawner if the spawner in the current lane has more than 95% health
	- Gold Rain if facing a Boss who has more than 60% health
- Respawns you after 5 seconds (instead of 1 minute) if you die
- Disables certain abilities and items if facing a Boss (to try to maximize Raining Gold and Metal Detector benefits)

## Installation ##

### Tampermonkey ###

1. Open Tapermonkey's dashboard.
2. Click on the `Utilities` tab on the right.
3. Paste `https://raw.githubusercontent.com/SteamDatabase/steamSummerMinigame/master/autoPlay.user.js` into the text area, and click `Import`.
4. When the editor has loaded, click `Install` (*NOT* `Process with Chrome`).

### Greasemonkey ###

1. Navigate to `https://raw.githubusercontent.com/SteamDatabase/steamSummerMinigame/master/autoPlay.user.js`.
2. Right click on the page, and click `Save Page As`.
3. While Firefox is still open, open a File Manager of any sort, and navigate to the directory you saved the script.
4. Drag & drop the script file onto the Firefox window.
5. Press `Install`.

### Manual ###

##### Chrome #####
1. Open https://raw.githubusercontent.com/SteamDatabase/steamSummerMinigame/master/autoPlay.user.js
2. Select All, Copy.
3. Navigate to `http://steamcommunity.com/minigame/` and join or start a game.
4. Press `Ctrl + Shift + J`.
5. Paste into the javascript input, and hit `Enter`.

##### Firefox #####
1. Open https://raw.githubusercontent.com/SteamDatabase/steamSummerMinigame/master/autoPlay.user.js
2. Select All, Copy.
3. Navigate to `http://steamcommunity.com/minigame/` and join or start a game.
4. Press `Ctrl + Shift + K`.
5. Paste into the javascript input, and hit `Enter`.

##### Internet Explorer / Microsoft Edge #####
1. Open https://raw.githubusercontent.com/SteamDatabase/steamSummerMinigame/master/autoPlay.user.js
2. Select All, Copy.
3. Navigate to `http://steamcommunity.com/minigame/` and join or start a game.
4. Press `F12` and navigate to the `Console` tab.
5. Paste into the javascript input, and hit `Enter`.

To stop the manual script, type `window.clearTimeout(window.SteamDB_Minigame_Timer);` into the console and hit `Enter`.

The game should now play itself, you should leave it running in the background. If you're not sure if it is auto-playing, try changing lanes. If it jumps back almost immediately, it's working.

## I want to contribute! ##

This project is open-source on github. There are different ways you can help:

- Find a Pull Request that's marked `needs testing`. Run that version of the script for a while and watch the console for errors. If there's no errors, pay attention to what the changes are doing gameplay-wise, and make sure it's doing what it's supposed to do.
- Find an Issue that's marked `help wanted`. Make the changes needed by that issue, and create a Pull Request with your enhancement or bugfix.
- Pick an item off the TODO list, below, and implement it. When it's done (and tested and working), create a Pull Request.
- Got an idea for an improvement that's not already listed? Code it up, test it out, then make a Pull Request when it's ready.
- Do NOT change the script version in your PR as it could be incremented before your PR is merged.
