# Framework Tanoa Life
This framework is a total modification for ArmA3 game.

## Requirements

### Mandatory
- Arma 3 server
- Database
- [extDB3](https://bitbucket.org/torndeco/extdb3/overview)
- [extLOG](https://github.com/Torndeco/extLOG)
- [Arma 3 framework addons](https://mega.nz/#!GEkACATR!iDuiZAuI2xuLEIZHk32F4YGHw9neC5gBjjClZFPUHq8)

### Useful links
- Server Start-up/Reboot management: [Batch file](https://www.altisliferpg.com/topic/2212-basic-bat-server-start)
- Database: [MySQL Server](https://dev.mysql.com/downloads/mysql)
- SQL Administration Tool: [HeidiSQL](https://www.heidisql.com/download.php)
- Text Editor: [Sublime Text 3](https://www.sublimetext.com/3)
- Command-line steam version: [SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD)

## Configuration
### Server side [-Link-](https://github.com/Lyeed/Framework_Tanoa_Life/blob/master/Tanoa-Server/configs/Config_Server.hpp)
### Staff members [-Link-](https://github.com/Lyeed/Framework_Tanoa_Life/blob/master/Tanoa-Life.Tanoa/configs/GameConfigs/Config_Staff.hpp)
### TaskForceRadio informations
##### initPlayerLocal [-Link-](https://github.com/Lyeed/Framework_Tanoa_Life/blob/master/Tanoa-Life.Tanoa/initPlayerLocal.sqf)
- Line 88 : Replace YOUR TEAMSPEAK NAME by your TeamSpeak's server name.  
`waitUntil {(["Lyeed Tanoa Life Teamspeak", (call TFAR_fnc_getTeamSpeakServerName)] call BIS_fnc_inString)};`

- Line 93 : Your channel name. Default: TaskForceRadio

##### fn_init_loops.sqf [-Link-](https://github.com/Lyeed/Framework_Tanoa_Life/blob/master/Tanoa-Life.Tanoa/core/Inits/fn_init_loops.sqf)
- Line 140: Specify all channels that players are allowed to visit while connected.  
`if (!((call TFAR_fnc_getTeamSpeakChannelName) in ["TaskForceRadio","MyNewChannel"])) then`

- Line 152: Replace YOUR TEAMSPEAK NAME by your TeamSpeak's server name.  
`if (!(["Lyeed Tanoa Life Teamspeak", (call TFAR_fnc_getTeamSpeakServerName)] call BIS_fnc_inString)) then`

### Database
- Execute the script [database](https://github.com/Lyeed/Framework_Tanoa_Life/blob/master/database.sql) on your SQL server.
- Modify ExtDB configuration file according to your needs:
```
[tanoa]//<--------------- IMPORTANT
IP = 127.0.0.1//<-------- CHANGE IF YOUR DATABASE IS NOT LOCAL
Port = 3306//<----------- DEFAULT MySQL PORT
Username = root//<------- DATABASE ACCOUNT WITH PRIVILEGES TO USE
Password =  *******//<--- DATABASE ACCOUNT PASSWORD. CHANGE IT
Database = tanoa//<------ IMPORTANT
```

## Author
* **Lyeed** - [Lyeed](https://github.com/Lyeed)

## License
For a human-readable version of the [project's license](https://github.com/Lyeed/Framework_Tanoa_Life/blob/master/LICENSE.md), see http://creativecommons.org/licenses/by-nc-nd/4.0/

## Bugs report
Please open an issue for any encountered bug, I will do my best to correct it.

If you are not familiar with the GitHub's issue system, please refer to [the documentation](https://guides.github.com/features/issues/)

## Pictures
![Tablet_1](https://cdn.discordapp.com/attachments/434398524269002784/435855164650553354/20180415121249_1.jpg)
![Tablet_2](https://i.imgur.com/2AVLsTF.jpg)
![Tablet](https://cdn.discordapp.com/attachments/434398524269002784/435855519756845056/20180417193330_1.jpg)
![Welcome](https://images-ext-2.discordapp.net/external/4BJgWyhu8Q1qYlNMlNiYtaZqZrPVWzWMh2Mcby_uPJw/https/i.imgur.com/dOSvgx5h.jpg)
![Inscription](https://steamuserimages-a.akamaihd.net/ugc/2434635842564505288/6BEE68FB5B8363C0DFC78EFB99648FD8B2954A50/)
![Company](https://i.imgur.com/k6WJiCI.jpg)
![Death](https://i.imgur.com/gNo7n4J.jpg)
![Stock](https://i.imgur.com/yYMOMdr.jpg)
![Military](https://i.imgur.com/ylNlNsn.jpg)
![Massage](https://i.imgur.com/0qUKHuG.jpg)
![Inventory](https://i.imgur.com/K40l9p3.jpg)
