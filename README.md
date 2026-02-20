# "Casualties: Unknown" Co-op mod by Krokosha666
(my abandoned YT channel): https://www.youtube.com/@Krokosha666<br>
A simple LAN Multiplayer Co-op Mod for Scav Prototype V5 Pretest 4<br>
Game link: https://orsonik.itch.io/scav-prototype<br>
Discord server for discussing this mod: https://discord.gg/SA6H7mA6De<br>
[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://buymeacoffee.com/krokosha666)

### Gameplay showcase: 
[![Video Title](https://img.youtube.com/vi/dvVuY3R9wV8/0.jpg)](https://www.youtube.com/watch?t=61&v=dvVuY3R9wV8)

# Automatic install:
1. [**danxnader**](https://github.com/danxnader/ScavKRInstaller) created an automatic installer tool for this mod:
    - [Download the ScavKRInstaller.exe](https://github.com/danxnader/ScavKRInstaller/releases/latest/download/ScavKRInstaller.exe)
    - Note: You can not play singleplayer with this version of the game.
2. Follow the tool's instructions.<br>It should install the correct game version for the latest version of this mod.



# Manual install:
<details>
  <summary>Click to show text guide.</summary>

## What you need

1. The game from:
    - ~~https://orsonik.itch.io/scav-prototype~~ public version is too new.
    - [ScavKRInstaller's Source](https://github.com/danxnader/ScavKRInstaller/blob/16cda961730556f0eec00ed3e3096f15c3575169/ScavKRInstaller/Constants.cs#L21-L23) has links to the version you'll need.

2. The mod from:
    - [This repo's release page](https://github.com/Krokosha666/cas-unk-krokosha-multiplayer-coop/releases)

3. BepInEx, a Unity mod loader, from:
    - [Their release page, specifically the v5 x64 version](https://github.com/BepInEx/BepInEx/releases), [v5.4.23.4](https://github.com/BepInEx/BepInEx/releases/download/v5.4.23.4/BepInEx_win_x64_5.4.23.4.zip) is known to work.
    - **Linux**: Casualties Unknown is a Windows executable, so you will still need the Windows version of BepInEx regardless; don't get the Linux version of BepInEx.

## Putting it together

1. Extract the game somewhere.

2. [Install BepInEx onto the game.](https://docs.bepinex.dev/articles/user_guide/installation/index.html#installing-bepinex-1)
    - Or tersely, extract the contents of the BepInEx zip next to the game's executable (`CasualtiesUnknown.exe`)

3. Create the path `BepInEx/plugins/cas-unk-mp` within the game directory.
    - Any name is fine in place of `cas-unk-mp`; it's for organization when [installing mods](https://github.com/05126619z/ChangeSkin).

4. From the mod zip, extract the contents of `BepInEx/plugin` to `BepInEx/plugins/cas-unknown-mp`
    - You should have a structure like this:
```
CasualtiesUnknown/
    CasualtiesUnknown.exe
    UnityPlayer.dll
    UnityCrashHandler64.exe
    CasualtiesUnknown_Data/
    MonoBleedingEdge/
    winhttp.dll ← From BepInEx
    BepInEx/
        core/
        plugins/cas-unk-mp/
            KrokoshaCasualtiesMP.dll
            Unity.Netcode.Runtime.dll
            Unity.Netcode.Components.dll
            Unity.Networking.Transport.dll
```

5. Start the game, dismiss the content warning, and a new dialog in the upper left should appear. Continue to [How to play](#how-to-play).
    - **Linux**: [Continue reading](#linux)

## Linux

You will need to use Wine or Valve's Proton (thru Steam or Bottles) to run Casualties Unknown. If you use Wine, consider [Bottles](https://usebottles.com/) or at least [Wine Prefixes](https://gitlab.winehq.org/wine/wine/-/wikis/FAQ#wineprefixes) to avoid headaches in the future.

You will also need to allow `winhttp` to be overriden:
* Bottles:
    1. Create your Casualties Unknown bottle with the Gaming preset
    2. Your Casualties Unknown bottle →
    3. Options ­– Settings
    4. Compatibility – DLL Overrides
    5. New Override: `winhttp` then 'Apply'
    6. Navigate the way back to your bottle
    7. 'Run Executable' against the executable to play now or 'Add Shortcuts...' for later.
* Proton:
    1. [Add a non-Steam game](https://help.steampowered.com/en/faqs/view/4B8B-9697-2338-40EC)
    2. Right-click the new Casualties Unknown entry
    3. Properties
    4. Compatibility
    5. 'Force the use of a specific Steam Play compatibility tool'
    6. Select a version of Proton
    7. Run the game once (to populate the prefix)
    8. [Follow BepInEx's guide](https://docs.bepinex.dev/articles/advanced/proton_wine.html)
* Wine Prefix:
    1. `WINEPREFIX=my-wine-prefix winecfg`
    2. [Add the override](https://docs.bepinex.dev/articles/advanced/proton_wine.html#2-configure-proxy-to-run)
    3. `WINEPREFIX=my-wine-prefix CasualtiesUnknown.exe`
* Wine: `WINEDLLOVERRIDES="winhttp=n,b" wine CasualtiesUnknown.exe`

For vanilla Wine, you might need Arial fonts. Check your distro's repository, `winetricks allfonts`, or find Arial.ttf and install it.
</details>
<br>

# How to play:
Lookup any Minecraft vLAN/LAN/Port-forwarding tutorial, it will work the same.<br>
(except that my mod doesn't scan your Local Network lol, you need to always input an IP address)<br>
(and also this mod uses UDP protocol instead of TCP)<br>

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
    - Expected input - 192.168.0.10:7790
    - IP - 192.168.0.10
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
Usernames and a simple text chat.<br>
Middle Mouse Button to point at a location.<br>
Right click to interact and heal other players.<br> 
Stay close to others to share body temperature.<br>
Spectator mode when dead.<br>
Sleeping is disabled.<br>
Carrying incapacitated players.<br>
Any dead players respawns at next layer.<br>
Unchipped option is individual.<br>
Most of these features can be tweaked in the in-game console. (type "krok help" to show)<br>

There's no client prediction.<br>
There's no network ownership.<br>
There's no deterministic RNG.<br>
There's no anticheat. <br>
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

You can eat your friends after they died.

Traders first impression reputation is calculated from the prettiest of the bunch.<br>



# How to enable cheats:

The Host must enter this console command:<br>
```krok rule sv_cheats 1```<br>
and then to allow clients to cheat:<br>
```krok rule AllowClientCheatCommands 1```<br>


















