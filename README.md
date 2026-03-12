# "Casualties: Together" Co-op Mod
Mod for an itch.io game "Casualties: Unknown" by Orsoniks<br>
Game link: https://orsonik.itch.io/scav-prototype<br>
LAN Multiplayer Mod made by Krokosha666<br>
(my abandoned YT channel): https://www.youtube.com/@Krokosha666<br>
Discord server for discussing this mod: https://discord.gg/SA6H7mA6De<br>
[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://buymeacoffee.com/krokosha666)

### Gameplay showcase: 
[![Scav Multiplayer](https://img.youtube.com/vi/dvVuY3R9wV8/0.jpg)](https://www.youtube.com/watch?t=61&v=dvVuY3R9wV8)

# Automatic install:
1. [**danxnader**](https://github.com/danxnader/ScavKRInstaller) created an automatic installer tool for this mod:
    - [Download the ScavKRInstaller.exe](https://github.com/danxnader/ScavKRInstaller/releases/latest/download/ScavKRInstaller.exe)
    - Note: You can not play singleplayer with this version of the game.
2. Follow the tool's instructions.<br>It should install the correct game version for the latest version of this mod.



# Manual install:
<details>
  <summary>Click to show text guide.</summary>

1. Download the game from:
- https://orsonik.itch.io/scav-prototype 

2. You have to copy the game again if you want to play singleplayer later.

3. Download the mod and unzip the contents into the game root directory.
    - Click the ["Code > Download Zip"](https://github.com/Krokosha666/cas-unk-krokosha-multiplayer-coop/archive/refs/heads/main.zip)

4. Unzip BepInEx zip into the game root directory (where the .exe is located).
    - Official download: [BepInEx_win_x64_5.4.23.5.zip](https://github.com/BepInEx/BepInEx/releases/download/v5.4.23.5/BepInEx_win_x64_5.4.23.5.zip)

5. Go to CasualtiesUnknown/BepInEx/plugins/   
   - (Launch the game once to create the "plugins" folder)
6. Copy and paste all dlls from "MultiplayerMod/BepInEx/plugins/" into there.
    - **Now your game root folder should look like this:**
    ```
    CasualtiesUnknown/
    - CasualtiesUnknown.exe
    - UnityPlayer.dll
    - UnityCrashHandler64.exe
    - CasualtiesUnknown_Data/
    - MonoBleedingEdge/
    - winhttp.dll  <-  from BepInEx zip
    - BepInEx/
    - - plugins/
    - - - KrokoshaCasualtiesMP.dll  <-  from mod zip
    - - - Unity.Netcode.Runtime.dll
    - - - Unity.Networking.Transport.dll
    - - - ...and so on
    - - core/
    ```
7. Launch the game by double clicking the CasualtiesUnknown.exe.

8. In main menu, multiplayer related buttons should appear.

9. Continue to "How to play" sections of this README.

<details>
<summary>FOR LINUX USERS</summary>

1. For Linux Wine you need to enable dll override for winhttp !!

    - cmd: `WINEDLLOVERRIDES="winhttp=n,b" wine CasualtiesUnknown.exe` 
    - But you should create a Wine profile for it to be permanent.

2. If you can't see text on the multiplayer menu you need to install wine fonts.
    - Download a random Arial.ttf off of the internet or run `winetricks allfonts`.
</details>
</details>
<br>



# How to play:
Lookup any Minecraft vLAN/LAN/Port-forwarding tutorial, it will work the same.<br>
(except that my mod doesn't scan your Local Network lol, you need to always input an IP address)<br>
(but this mod uses UDP protocol instead of TCP)<br>

known good vLAN software: ZeroTier, Radmin VPN, Tailscale, Hamachi 


(i will only cover Radmin VPN side of things, same applies to other vLAN software)<br>
Install RadminVPN from https://www.radmin-vpn.com/


## How to host:
1. Install Radmin VPN.
2. Create Network, name it anything.
3. Run game and enter the Main Menu.
4. IP:PORT can stay default.
5. Password is optional.
6. Press the big "Start Host" button.
7. If your OS Firewall prompts you about it, click "Allow".
8. Wait for your friends to connect.
9. Press "Start Run" or "Tutorial" button. Everyone should go into load screen and then spawn in the world.
10. Now become casualties yall.
11. (optional) Upvote and support the mod.


## How to join:
1. Install Radmin VPN.
2. In Radmin VPN, join the Host's network.
3. Right click on your Host and press "copy IP".
4. Run game and enter the Main Menu.
5. Ask Host for their password (if there's none, leave it empty).
6. Ask Host for their PORT number.
7. Paste IP and write PORT in the textbox, example:
    - Expected input - 21.168.0.10:7790
    - IP - 21.168.0.10
    - PORT - 7790
    - Make sure there's colon inbetween them.
8. Press the big "Client Connect" button.
    - If it fails to connect make sure the game is whitelisted in your OS Firewall settings, and do other troubleshooting.
9. (optional) Upvote and support the mod.

    
# Warning:
If nothing works: It's a skill issue - Don't whine and try again.
 - Or cry at people in "Casualties: Together" discord server: https://discord.gg/SA6H7mA6De

Also, restart the game after disconnect or failed attempt, to reset for sure.

!!!<br>
IF YOU ENCOUNTER ANY GLITCHES, CRASHES, OTHER ISSUES - BLAME ME AND THE MOD, NOT THE ORIGINAL DEVELOPER OF THE GAME<br>
!!!



# Features:
Usernames and a text chat.<br>
Real voice chat with in-game effects.<br>
Middle Mouse Button to point at a location.<br>
Right click to interact and heal other players.<br> 
Stay close to others to share body temperature.<br>
Spectator mode when dead.<br>
Sleeping is disabled.<br>
Hunger and thirst is slowed down.<br>
Carrying incapacitated players.<br>
Any dead players respawns at next layer.<br>
Unchipped option is individual.<br>
Most of these features can be tweaked in the in-game console.<br>
Also this mod can run as a dedicated server.<br>

There's no client prediction.<br>
There's no network ownership.<br>
There's no deterministic RNG.<br>
There's no anticheat. <br>
This mod only adds a simple co-op experience to the game.<br>






# FULL LIST OF FEATURES DIFFERENT FROM THE MAIN GAME:

Disabled sleeping. (tied to the rule "EnableSleep" )<br>
Disabled time scale buttons. (don't try re-enable this actually)<br>
Player friendly fire can be enabled with the "FriendlyFire" rule.<br>
Middle mouse click to highlight a location at your cursor, for the other players to see.<br>
Stand close to other players to share body temperature.<br>
Minigames like Keypad are also co-op, where you see others players inputs.<br>

Tutorial works as it should in multiplayer.<br>
Unchipped is individual. ( rule "UnchippedIsIndividual" )<br>
Text chat and Voice chat are dependent on your characters ability to speak, same distortions apply to your messages.<br>
MP3 Player now is a boombox instead of replacing background music.<br>

Right click on a player to open a player interaction context menu.
 - Inspect health panel and perform any actions.
 - Inspect their inventory and take their items. (if rule "CanAccessOthersInventory" is false you can only access inventory of an unconscious player)
 - Feed any food or any usable item, like AutoPump.

When a player dies, they are put into spectator mode.
 - All dead players respawn after living players reach the next level.
 - (if rule "Permadeath" is true, respawns are disabled)

To continue to the next layer, half of all players must reach the end. 
 - Straggles will get killed if they take too long.
 - Only the Host gets prompted to continue the run.
 - DrillPod works the same, all players must be in the pod to continue.
 - (tweaked by the rule "LayerFinishConditionPlayerPercent")

Slowed down hunger and thirst ( rule "MetabolismMultiplier")<br>
Player health regen and decay is tweaked.
 - Death is much faster if there are no comrades nearby. ( tweaked by the "AdditionalHealthDecay" rule )
 - Health regeneration is boosted. ( tweaked by the "AdditionalHealthRegen" rule)

All these rules can be changed only by the Host by running the command "rule [rule name] [new value]"<br>

You can eat your friends after they died. 
 - The rule "CanAmputateHealthyPlayers" allows you to steal limbs of living players.

Traders first impression reputation is calculated from the prettiest of the bunch.<br>



# How to enable cheats:

The Host must enter this console command:<br>
```rule sv_cheats 1```<br>
**To let Client into server console mode they need "admin" privilege.**<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**(Given by "adminpriv [player]" or "adminpriv-password")**
















