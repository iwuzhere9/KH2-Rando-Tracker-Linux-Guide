# KH2 Randomizer Additional Tools Setup for Steam Deck

> [!IMPORTANT]
> - This guide was built specifically for Steam Deck users, so if you're on another Linux distro, you may have to play around with more things to get it all running smoothly.
> - You will have to switch to Desktop Mode and use a mouse and keyboard, an external display is HIGHLY recommended but everything is possible on the Deck itself.

If you need to get the Mods Manager and Seed Generator set up, please consult the [wonderful guide](https://github.com/KHOmega/KH-PC-and-Linux-Setup/blob/main/GoA-Randomizer-linux-setup.md) by [KHOmega](https://github.com/KHOmega) 

This guide is to help Steam Deck users get set up at parity with Windows installs for the tools to use when playing Randomized Seeds, and to ensure that they are capable of joining in any races or tournaments the community puts together. 

If there are any big changes after any updates to the Tracker or Livesplit, I'll do my best to keep this guide up to date. 

# KH2 Rando Tracker 

The KH2 Rando Tracker isn't a mod but instead a full fledged automated tracker program for the Important Checks in game. Instead of having to open Jiminy's Journal to get a hint for progression, the Tracker will have it all listed in an easy to parse grid showing what unlocks are in which world. For more information on the different ways to play, check out the [Hint Systems](https://kh2rando.com/hints) page from the Randomizer website.

- Step 1: Go to the [GitHub page](https://github.com/Dee-Ayy/KH2Tracker/releases/latest) and download the most recent release of the Tracker

- Step 2: In Steam, you will change the `Launch Options` from what was listed earlier to `STEAM_COMPAT_LAUNCHER_SERVICE=proton WINEDLLOVERRIDES="version,dinput8=n,b" %command%`

- Step 3: Launch the game with the seed installed, and then choose `New Game` before moving to another window to keep the intro movie from playing. 

- Step 4: Run the following command in terminal after starting the game:
    `/path/to/steamapps/common/SteamLinuxRuntime_sniper/pressure-vessel/bin/steam-runtime-launch-client \ --bus-name=com.steampowered.App2552430 -- wine /path/to/KhTracker.exe`

For the command to work and not be read as two separate commands, you will want to replace the space between " \ " and "--bus" with a line break. Use Kate or whatever text editor you prefer to make the changes as you won't have the same freedom within the terminal window to handle any changes to the path or formatting.

You will also need to actually enter the file paths for steam-runtime-launch-client and KhTracker.exe rather than keeping it as "/path/to/" 

- Step 5: You should see the terminal working, and after a short moment the Tracker itself should open up. Under `Options` you will want to click `Hint Loading...` and then `Load KH2 Randomizer Seed (*.zip)`

- Step 6: If you have the seed hash show up in the Tracker window, you can click `Options` and then `Start Auto-Tracking` so the game will automatically keep track of what Important Checks you have found. If the bottom right of the window shows a green PC, then it has opened correctly and is tracking your game!

# Livesplit

If you want to see how fast you think you can clear a seed or want to join in any of the races on the Rando Discord server, the last step you'll need is getting Livesplit set up. 

- Step 1: Download the most recent stable build of Livesplit from their [website](https://livesplit.org/downloads/)

- Step 2: In Steam, change the `Launch Options` from what was listed earlier to `STEAM_COMPAT_LAUNCHER_SERVICE=proton WINEDLLOVERRIDES="version,dinput8=n,b" %command%`. If you follow the above steps for the Tracker, you don't need to change anything further.

- Step 3: Launch your randomized seed either through Steam or the Mods Manager, and hold the game on the `New Game` screen. 

- Step 3: Run the following command in terminal after starting the game:
    `/path/to/steamapps/common/SteamLinuxRuntime_sniper/pressure-vessel/bin/steam-runtime-launch-client \ --bus-name=com.steampowered.App2552430 -- wine /path/to/Livesplit.exe`

For the command to work and not be read as two separate commands, you will want to replace the space between "\" and "--bus" with a line break. You will also need to actually enter the steam-runtime-launch-client and Livesplit.exe rather than keeping it as "/path/to/"  

- Step 4: Next, you will want to get the Randomizer Load Remover for Livesplit from the [GitHub page](https://github.com/aliosgaming/KH2FM_Load_Remover-FOR-RANDOMIZER). The readme gives instructions on both an automated and manual install. The automated option is recommended, but if you have any issues then try to set up a fresh cooy of Livesplit using the manual instructions. 

- Step 5: Once the Load Remover has been set up, the timer will start on its own once you proceed through the options for setting up a New Game, and the timer will automatically stop once you defeat Final Xemnas, or the boss replacing him if you have boss randomizer enabled. 

# Credits

I take zero credit for any of the information here, I just pulled together what was put out and worked into a unified guide.

A MASSIVE thanks goes to [baili0411](https://github.com/baili0411) for figuring out how to get the Tracker and Livesplit working on the Steam Deck. 

Another huge shoutout goes to [KHOmega](https://github.com/KHOmega) for maintaining the Linux guides that let me and many others join the rando scene.

Lastly, a big thank you to all the contributors for the Randomizer and Guide on the [main page](https://tommadness.github.io/KH2Randomizer) for the Randomizer. 

If anything breaks or if you have any issues, sound off in the KH2 Rando discord and we should be able to help or update the guide as needed
