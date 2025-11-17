# "Casualties: Unknown" Co-op mod by Krokosha666
(my abandoned YT channel): https://www.youtube.com/@Krokosha666<br>
A simple LAN Multiplayer Co-op Mod for Scav Prototype V5 Pretest 4<br>
Game link: https://orsonik.itch.io/scav-prototype
Discord server for discussing this mod: https://discord.gg/SA6H7mA6De


# How to install:
1. Download the game from:
    - https://orsonik.itch.io/scav-prototype 

2. You have to copy the game again if you want to play singleplayer later.

3. Download the mod and unzip the contents into the game root directory.
    - Click the "Code > Download Zip"
    - Or heres direct link: https://github.com/Krokosha666/cas-unk-krokosha-multiplayer-coop/archive/refs/heads/main.zip

4. Unzip BepInEx_win_x64_5.4.23.3.zip into the game root directory (where the .exe is located).
    - Official download: https://github.com/BepInEx/BepInEx/releases/download/v5.4.23.3/BepInEx_win_x64_5.4.23.3.zip

5. Go to CasualtiesUnknown/BepInEx/plugins/   (create the plugins folder if its missing)
6. Copy and paste all dlls from "MultiplayerMod/BepInEx/plugins/" into there.

 - **Now your game root folder should look like this:**
 - -  CasualtiesUnknown/
 - - - CasualtiesUnknown.exe
 - - - UnityPlayer.dll
 - - - UnityCrashHandler64.exe
 - - - CasualtiesUnknown_Data/
 - - - MonoBleedingEdge/
 - - - winhttp.dll
 - - - BepInEx/
 - - - - plugins/
 - - - - - KrokoshaCasualtiesMP.dll
 - - - - - Unity.Netcode.Runtime.dll
 - - - - - Unity.Netcode.Components.dll
 - - - - - Unity.Networking.Transport.dll
 - - - - core/

7. Try to launch the game by double clicking the CasualtiesUnknown.exe.
    - LINUX WINE ONLY:
    - - For Linux Wine you need to enable dll override for winhttp !!
    - - cmd: `WINEDLLOVERRIDES="winhttp=n,b" wine CasualtiesUnknown.exe` 
    - - But you should create a Wine profile for it to be permanent.

8. In main menu, multiplayer related buttons should appear on top left corner of the screen.
    - LINUX WINE ONLY:
    - - If you can't see text you need to install wine fonts.
    - - Download a random Arial.ttf off of the internet or run `winetricks allfonts`.

9. Continue to "How to play" sections of this README.
 



# How to play:
Always confirm that you and your friends have the same game version, and the same mod version. (otherwise it all will break)<br>
Lookup any Minecraft vLAN/LAN/Port-forwarding tutorial, it will work the same.<br>
(except that my mod doesn't scan your Local Network lol, you need to always input an IP address)<br>
(and also this mod uses UDP protocol instead of TCP)<br>

known good vLAN software: ZeroTier, Radmin VPN, Hamachi 


(i will only cover Hamachi side of things, same applies to other vLAN software)

## How to host:
1. Make sure Hamachi is setup correctly and you see your friends with green light.
2. Run game and enter the Main Menu.
3. IP doesn't matter, you can change PORT if you want to.
4. Password is optional.
5. Press the big "Start Host" button.
6. If your OS Firewall prompts you about it, click "Allow".
7. Wait for your friends to connect.
8. Press "Start Run" or "Tutorial" button. Everyone should go into load screen and then spawn in the world.
9. Now become casualties yall.
10. (optional) Upvote and support the mod.


## How to join:
1. Make sure Hamachi is setup correctly and you see your friends with green light.
2. In Hamachi, right click on your Host and press "copy IP".
3. Run game and enter the Main Menu.
4. Ask Host for their password (if theres none, leave it empty).
5. Ask Host for their PORT number.
6. Paste IP and write PORT in the textbox, example:
    - Expected input - 192.168.0.10:7790
    - IP - 192.168.0.10
    - PORT - 7790
    - Make sure theres colon inbetween them.
7. Press the big "Client Connect" button.
    - If it fails to connect make sure the game is whitelisted in your OS Firewall settings, and do other troubleshooting.
8. (optional) Upvote and support the mod.

    
# Warning:
If nothing works: It's a skill issue - Don't whine and try again.
 - You can look up online any troubleshooting tutorials for any LAN game, same network issues apply to ALL software in the world.
 - Or better yet, go ask an AI about it. It's pretty good at troubleshooting network issues.
 - Or people at "Casualties: Together" discord server may help you: https://discord.gg/SA6H7mA6De

Also, restart the game after disconnect or failed attempt, to reset for sure.

!!!<br>
IF YOU ENCOUNTER ANY GLITCHES, CRASHES, OTHER ISSUES - BLAME ME AND THE MOD, NOT THE ORIGINAL DEVELOPER OF THE GAME<br>
!!!



# Features:
Usernames and a simple text chat.<br>
Middle Mouse Button to point at a location.<br>
Right click to interact and heal other players.<br> 
Stay close to others to share body temperature.<br>
Spectator mode when dead.<br>
Sleeping is disabled.<br>
Any dead players respawns at next layer.<br>
Unchipped option is individual.<br>
Most of these features can be tweaked in the in-game console.<br>
The mod is not nearly finished yet!<br>
More true co-op features are coming soon!<br>


# Features for nerds:
Added MP-specific console commands. (type "krok help" to show)<br>
This mod uses Unity Netcode as the networking library.<br>
Complete player and interactions synchronization.<br>
All in-game POIs and Items are synchronized.<br>
Simple world synchronization. (tiles and fluids)<br>
Janky physics synchronization.<br>
Theres no client prediction.<br>
Theres no network ownership.<br>
Theres no deterministic RNG.<br>
Theres no anticheat. <br>
This mod only adds a simple co-op experience to the game.<br>






# FULL LIST OF FEATURES DIFFERENT FROM THE MAIN GAME:

Disabled sleeping. (tied to the rule "DisableSleep" )<br>
Disabled time scale buttons. (tied to the rule "DisableTimeManipulation" )<br>
Player friendly fire can be enabled with the "FriendlyFire" rule.<br>
Middle mouse click to highlight a location at your cursor, for the other players to see.<br>
Stand close to other players to share body temperature.<br>
Minigames like Keypad and Lockpicking are also Co-op, where you see others players inputs.<br>

Tutorial works as it should in multiplayer.<br>
Unchipped is individual. (tied to the rule "UnchippedIsIndividual" )<br>
Text chat is dependent on your characters ability to speak, same distortions apply to your messages. (tied to the rule "SpeechImpairedTextChat" )<br>

Right click on a player to open a player interaction context menu.
 - Inspect health panel and perform any actions.
 - Inspect their inventory and take their items. (if rule "CanAccessOthersInventory" is false you can only access inventory of an unconscious player)
 - Feed any food or any usable item, like AutoPump.

When a player dies, they are put into spectator mode.
 - All dead players respawn after living players reach the next level.
 - (if rule "Permadeath" is true, respawns are disabled )

To continue to the next layer, all players must reach the end. 
 - Only the Host gets prompted to continue the run.
 - DrillPod works the same, all players must be in the pod to continue.
 - (if rule "ForNextLayerAllMustReachEnd" is false any player can reach the end alone, and drillpods work immidietly)

Player health regen and decay is tweaked.
 - Death is much faster if there are no conscious players nearby. (tweaked by the "AdditionalHealthDecay" rule )
 - Health regeneration is boosted. (tweaked by the "AdditionalHealthRegen" rule )

All these rules can be changed only by the Host by running the command "krok rule [rule name] [new value]"   <br>
Run "krok rule sv_cheats true" to enable console 'cheat' commands<br>

With friendly fire enabled, other players do a scared face if you aim your gun at them.<br>

Traders first impression reputation is calculated from the prettiest of the bunch.<br>



# How to enable cheats:

The Host must enter this console command:<br>
```krok rule sv_cheats 1```<br>
and then to allow clients to cheat:<br>
```krok rule AllowClientCheatCommands 1```<br>















