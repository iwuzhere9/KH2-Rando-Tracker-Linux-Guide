# KH2 Rando Steam Deck Setup Guide

> [!IMPORTANT]
> - This guide assumes you are installing this on Steam Deck! For other OS's, please adjust accordingly. 
> - This guide also assumes that you have some knowledge in how to navigate Linux based OSs!
> - Please launch into Desktop Mode and use a mouse and keyboard! While this is doable without a mouse or keyboard, it will be frustrating!
> - This guide is based on the [excellent guide](https://github.com/KHOmega/KH-PC-and-Linux-Setup/blob/main/refined-steam-linux-setup.md) by the Re:Fined team for their mod, as well as the [main guide](https://tommadness.github.io/KH2Randomizer/setup/Panacea-ModLoader/) for Randomizer setup the community has put together. Tracker and Livesplit on Linux is possible thanks the work of one of the KH2 Rando Discord members. 

## Prerequisites
To get started you need to download and install the following:

- [**KINGDOM HEARTS -HD 1.5+2.5 ReMIX-**](https://store.steampowered.com/app/2552430/KINGDOM_HEARTS_HD_1525_ReMIX/)
   - This guide assumes you have the game downloaded to your ***Internal Storage***.
   - If not, please symlink it to your Internal Storage's game directory.
      - [eg: `path/to/location/in/sdcard/` -> `~/.local/Steam/steamapps/common/KINGDOM HEARTS -HD 1.5+2.5 ReMIX-/`]
   - Ensure that you've run the game at least once before getting any mods installed, and add `WINEDLLOVERRIDES="version,dinput8=n,b" %command%` to the `Launch Options` in Steam.


- [**OpenKH**](https://github.com/OpenKH/OpenKh/releases)
   - Will be downloaded from the `OpenKHSetup.sh` Script

- **Seed Generator**
   - The generator can be downloaded using [this link](https://tommadness.github.io/KH2Randomizer/setup/Panacea-ModLoader/) from the Randomizer setup page.

- **Protontricks (Flatpak)**
   - Download from Discover and run once.

- Password set in Konsole
   - Enter `passwd` in Konsole to setup a password if you haven't already.

# Setting Up OpenKH's Prefix

- Step 1: In Konsole, enter and run the following code:
  - `wget https://raw.githubusercontent.com/KHOmega/KH-PC-and-Linux-Setup/refs/heads/main/refined_specific/OpenKHSetup.sh -O - | sh`
  - You can instead download the files directly from [this link](https://github.com/OpenKH/OpenKh/releases/download/latest/openkh.zip) if you don't want to use Konsole and can extract the folder manually. The path for the next step would change depending on your choice here, but nothing else would be effected.

- Step 2: In Steam, click `Add a Game` on the bottom right, select `Add a Non-Steam Game...`, select `Browse`, navigate to `~/Documents/OpenKH`, select `OpenKH.Tools.ModsManager.exe`, and click `Open`. Then click `Add Selected Programs`.

![OpenKH Steam Library](https://github.com/user-attachments/assets/6b7af2e3-3d06-4acb-9e02-2c0f1003c58f)

- Step 4: Right Click `OpenKH.Tools.ModsManager.exe` in your Steam Library, and click `Properties`
   - Click `Compatibility`, and then select `Force the use of a specific Steam Play compatibility tool`, and select `Proton Experimental`
   - Optional: Rename `OpenKH.Tools.ModsManager.exe` to something more cleaner such as `OpenKH Mods Manager` in the properties window.

- Step 5: Load up OpenKH. This will generate a prefix and it will error out telling you that **.NET 6** needs to be installed. Select `No` and proceed to the next step.

- Step 6: Navigate to your `Downloads` folder and open `windowsdesktop-runtime-6.0.31-win-x64.exe`.
   - Protontricks should now open up. When it does, locate OpenKH on the game selection and select it to install **.NET 6** to its prefix.

- After a couple minutes, open OpenKH Mods Manager again and proceed with the tutorial.

# Setting up OpenKH:

> [!IMPORTANT]
> - You will need to set up OpenKH on the system storage and not an external drive, though you can have the actual game installed externally and still use the randomizer and other mods without any major issues. Guide author has not personally tested moving the install from system storage after extracting, but with making sure everything works smoothly

- Step 1: A window will pop up saying "Welcome to OpenKH Mods Manager".

  On the `Welcome to OpenKH Mods Manager` screen, click `Next >`, then under `Game edition`, select `PC Release`, then select `Global`, and then `Steam` under the next two opions.

  Select `Detect Installations`. If this fails to find where your game is installed, please manually find the folder where the game is installed
  - This is usually located in `Z:\home\deck\.local\share\Steam\steamapps\common\KINGDOM HEARTS -HD 1.5+2.5 ReMix-`

- Step 5: Click `Next >` and choose `Install Panacea`. Make sure the the Game Collection drop-down menu is set to `KINGDOM HEARTS 1.5 + 2.5 ReMIX`
   - OpenKH Panacea allows you to load your mods without modifying the game files.

- Step 6: OpenKH will ask if you want to install `Lua Backend`. After again confirming you have the Game Collection set to `KINGDOM HEARTS 1.5 + 2.5 ReMIX`

  Ensure that the `KH2` checkbox is enabled then click `Install and Configure Lua Backend` 

  After the install is complete, click `Next`

- Step 7: - On the next screen, it will ask if you want to `Launch Games Directly (Steam)`. Skip this, as this method does not work on Steam Deck/Linux.

- Step 8: Make sure `KH2-43GB` is checked, and then click `Extract game data`. This may take roughly *thirty* or more minutes.
   - If you encounter any errors extracting the game files, please either try again, or re-download your game!

- Step 9: After extraction, click `Next >` and then click `Finish`

When you are done, you should be at this screen!

![image](https://github.com/KHOmega/KH-Linux-Setup/assets/93887977/3c0d26c6-1ef5-4f3e-ba84-9e29a8e0291a)

# Garden of Assemblage Mod Installation:

The first mod and one of the constants for use in Randomizer will be the Garden of Assemblage mod. Getting mods installed is fairly easy after you've got everything set up. 

- Step 1: Be sure the game selected in the top right of the Mods Manager main window shows `Kingdom Hearts 2`

- Step 2: Next, Click `Mods` in the top left drop down menu, and then client `Install a new mod` 

![image](https://tommadness.github.io/KH2Randomizer/setup/images/Panacea-ModLoader/Install%20New%20Mod.png)

- Step 3: In the `Add a new mod from GitHub` section, type in `KH2FM-Mods-Num/GoA-ROM-Edition`. This will download the GoA mod from its hosted GitHub repo
   - ****You can find more mods posted in the KH2 Rando Discord Server [here](https://discord.com/channels/712837252279173150/975234023926399027)****

![image](https://tommadness.github.io/KH2Randomizer/setup/images/Panacea-ModLoader/Install%20GoA%20ROM.png)

- Step 4: To enable GoA, be sure to click the checkbox next to the newly add mod in the list

![image](https://tommadness.github.io/KH2Randomizer/setup/images/Panacea-ModLoader/Enable_GoA_ROM.png)

- Step 5: Once you have all the mods you want to use installed, click `Mod Loader` and then `Build and Run` which will build your mods and run the game for you automatically. Be sure to keep the GoA mod at the bottom of the active mod list and your randomizer seed at the top of the active list. 

# Installing a new seed to play:

- Step 1: You will want to follow the steps from the earlier section for `Setting Up OpenKH's Prefix` but using `KH2.Randomizer.exe` instead of the mod manager program.

- Step 2: Open the Seed Generator app from Steam. The first time will take some time to open as it extracts the necessary folders and files it uses, and it can take some time to process on subsequent uses, but so long as it is still listed as running in Steam, there isn't anything to worry about. 

- Step 3: Choose your seed settings in the generator window, or choose one of the built in presents under the `Preset` tab and then click on `Generate Seed` on the bottom right. Certain options will cause the button to be broken out for PCSX2 and the PC version, so make sure you are generating the corrrect format. 

- Step 4: This will open up a window to save the seed as a zip file. Save it in a location you can easily access through the Windows layer of the file explorer. 

- Step 5: Once saved, open the Mods Manager again and click on `Mods`, then `Install a New Mod`

- Step 6: This time click on `Select and Install Mod Archive or Lua Script`, navigate to your new seed zip file and click `Open`

- Step 7: Be sure to click on the check box next to the seed, and that it is sitting at the top of the mod list. Then click on `Mod Loader` and then `Build and Run` to enable the mod in game. 

![image](https://tommadness.github.io/KH2Randomizer/setup/images/Panacea-ModLoader/Enable%20New%20Seed.png)

The five buttons on the right are to help manage mods. The first button places a mod at the top of the list. The second moves a mod up the list one space, the third moves it down the list by one space. The green "+" icon is a shortcut to install a new mod, while the red “-“ icon is a shortcut to deleting a mod

To install a new seed, you would Delete the existing seed from your Mods Manager, and then install the new seed in the same way you did before. If you use the default seed name, you will receive a warning that a mod of the same name exists already, which you can proceed through. When selected, the right side of the manager will show you the seed hash, a series of symbols which is also displayed in the Seed Generator and in game as you start a new file. Ensure that these match throughout the process. 

# Recommended Mods

To start, the following mods are **highly** recommended to help navigate any crashes or soft-locks you may run into. 

****`KH2FM-Mods-equations19/auto-save` - This mod auto saves the game for you as you enter rooms. Be sure to make at least 1 regular save in game, then if you ever crash or your game closes unexpectedly, just hold the SELECT button while loading a save, and the auto-save will be loaded instead.****

****`KH2FM-Mods-equations19/soft-reset` - Hold L1+L2+R1+R2+Start at the same time to immediately reset the game to the start screen. Very useful if you accidentally softlock in boss/enemy rando, or just to restart the game faster!****

****`KH2FM-Mods-equations19/KH2-Lua-Library` - This mod is required to use either of auto-save or soft-reset.****

![image](https://tommadness.github.io/KH2Randomizer/setup/images/Panacea-ModLoader/Final%20View.png)

That's everything for the basic setup, so if you just want to explore the Randomizer, this is the last step that is needed! If you don't need any additional tools and just want to relax, you can exit Desktop Mode and launch the 1.5 + 2.5 Collection to play the randomizer in a standard mode. If you are looking to use the Tracker, Livesplit, or keep Discord active, then you'll need to stay in Desktop Mode and keep reading below. 

# KH2 Rando Tracker 

The KH2 Rando Tracker isn't a mod but instead a full fledged automated tracker program for the Important Checks in game. Instead of having to open Jiminy's Journal to get a hint for progression, the Tracker will have it all listed in an easy to parse grid showing what unlocks are in which world. For more information on the different ways to play, check out the [Hint Systems](https://kh2rando.com/hints) page from the Randomizer website.

- Step 1: Go to the [GitHub page](https://github.com/Dee-Ayy/KH2Tracker/releases/latest) and download the most recent release of the Tracker

- Step 2: In Steam, you will change the `Launch Options` from what was listed earlier to `STEAM_COMPAT_LAUNCHER_SERVICE=proton WINEDLLOVERRIDES="version,dinput8=n,b" %command%`

- Step 3: Launch the game with the seed installed, and then choose `New Game` before moving to another window to keep the intro movie from playing. 

- Step 4: Run the following command in terminal after starting the game:
    `/path/to/steamapps/common/SteamLinuxRuntime_sniper/pressure-vessel/bin/steam-runtime-launch-client \ --bus-name=com.steampowered.App2552430 -- wine /path/to/KhTracker.exe`

For the command to work and not be read as two separate commands, you will want to replace the space between "\" and "--bus" with a line break. You will also need to actually enter the steam-runtime-launch-client and KhTracker.exe rather than keeping it as "/path/to/" 

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

- Step 4: Next, you will want to get the Radnomizer Load Remover for Livesplit from the [GitHub page](https://github.com/aliosgaming/KH2FM_Load_Remover-FOR-RANDOMIZER). The readme gives instructions on both an automated and manual install. At this time, there isn't enough data to see which is the preferred way or if one is an instant error, so I'd recommend following the automated instructions first before trying manual. 

- Step 5: Once the Load Remover has been set up, the game will start automatically once you proceed through the options for setting up a New Game, and the timer will automatically stop once you defeat Final Xemnas, or the boss replacing him if you have boss randomizer enabled. 

# Credits

I did the easy part of stitching things together, so the most credit I can take is being bored at work and compiling things. 

A MASSIVE thanks goes to a user on the KH2 Rando Discord for figuring out how to get the Tracker and Livesplit working on the Steam Deck. (Waiting for a reply from the user before throwing their name out unwanted) 

Another huge shoutout goes to [KHOmega](https://github.com/KHOmega) for maintaining the Re:Fined guide that has been the backbone of getting Rando running on the Deck along with the rest of the Re:Fined team for making a STELLAR mod 

Lastly, a big thank you to all the contributors for the Randomizer and Guide on the main website. 
