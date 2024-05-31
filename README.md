# Counter-Strike Source Dedicated Surf Practice Server
This is a collection of addons, maps, scripts, and configuration files used for my personal surf server.
![](https://i.imgur.com/h14bOsV.png)
The server contains the following, already configured for your convenience:
- [Influx Timer](https://influxtimer.com/) and [predefined zones](https://github.com/Sayt123/SurfZones)
- [Metamod and Sourcemod](https://www.sourcemod.net/)
- Some preinstalled maps
## Installation Guide
### Setting up the server
- This guide assumes you're hosting this from a Windows machine.
- Download [SteamCMD](https://steamcdn-a.akamaihd.net/client/installer/steamcmd.zip).
- Note that the folder containing the SteamCMD executable will be the folder in which your server is stored.
- In the command prompt, login anonymously: `login anonymous`.
- Install the CS:GO dedicated server: `app_update 232330 validate'.
- Exit SteamCMD.
- Navigate to the folder containing your dedicated server, containing the folders: `bin`, `hl2`, `cstrike`, and `platform`.
- From this repository, remove the `start.bat` and `Server.cfg` files located inside `!PUT THESE NEXT TO CSTRIKE FOLDER NOT IN IT` and place them next to the `cstrike` directory in your dedicated server (the file will exist alongside the 4 folders I just mentioned).
- For some reason, I've been experiencing issues unless you copy the maps folder from the server's `cstrike` folder into your own client-side `Counter-Strike Source/cstrike` folder (In Steam, right click CSS -> Manage -> Browse local files to access this folder).
- In your dedicated server, navigate to `cstrike/addons/sourcemod/configs` and open the file `admins_simple.ini`.
- Use [steamidfinder.com](https://www.steamidfinder.com/) to find your Steam ID, for example, mine is `STEAM_0:0:47800602`.
- Replace this Steam ID in the configuration file with your own.
- To adjust the server's configuration, modify files in `cstrike/addons/sourcemod/configs` and `cstrike/cfg`, as well as `start.bat` and `server.cfg`.
### Starting the server
- Run `start.bat` to start your local server.
- Open the community server browser and go to the Local Games tab, where your server will appear.
- Join and have fun! Consider binding keys to `"say !COMMAND"`, where `COMMAND` could be `usp`, `knife`,`maps`, and `admin`(to configure the server/timer settings).
- I'd recommend binding mouse3 to `sm_restart` or `sm_teleport`, allowing you to restart your run whenever you'd like.
- Have fun!
### Installing new maps
- To add your own maps, download the .bsp files and place them in the `cstrike/maps` folder
- You'll probably need to put them in your own client's map folder as well (`Counter-Strike Source/cstrike`)
- Edit `cstrike/cfg/mapcycle.txt`, adding the names of each map you've installed (without `.bsp` at the end).
- Restart your server if it's already running.
- Finally, use the chat command `!maps` to select a map.
- Also, keep in mind that not all of the maps will have zones, which might break `sm_restart`.