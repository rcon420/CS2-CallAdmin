# CS2 CallAdmin
Plugin for CS2 that reports a player on game and send a webhook message to discord.
Admins can handle the report by marking it as handled. `(optional)`
All reports are stored in the database. `(optional)`

## Installation
1. Install **[CounterStrike Sharp](https://github.com/roflmuffin/CounterStrikeSharp/releases)** and **[Metamod:Source](https://www.sourcemm.net/downloads.php/?branch=master)**;
3. Download **[CallAdmin](https://github.com/1Mack/CS2-CallAdmin/releases)**;
4. Unzip the archive and upload it into **`csgo/addons/counterstrikesharp/plugins`**;

## Config
The config is created automatically. ***(Path: `csgo/addons/counterstrikesharp/configs/plugins/CallAdmin`)***
```
{
  "Version": 7,
  "ServerIpWithPort": "",
  "CooldownRefreshCommandSeconds": 30,
  "Reasons": "Hack;Toxic;Camping;Your Custom Reason{CUSTOMREASON}",
  "WebHookUrl": "",
  "Debug": true,
  "Database": {
    "Host": "",
    "Port": 3306,
    "User": "",
    "Password": "",
    "Name": "",
    "Prefix": "call_admin"
  },
  "Commands": {
    "ReportPrefix": "report",
    "ReportPermission": "",
    "ReportHandledEnabled": true,
    "ReportHandledPrefix": "report_handled",
    "ReportHandledPermission": "@css/generic;@css/ban"
  },
  "Embed": {
    "ColorReport": 16711680,
    "ColorReportHandled": 65280
  },
  "ConfigVersion": 7
}
```
## Commands
- **`report`** - Reports a Player; **(`#css/admin` group is required for use)**
- **`report_handled [identifier]`** - Mark a report as handled; **(`@css/generic;@css/ban` flag is required for use)**

## Translations
You can choose a translation on the core.json of counterstrikesharp or type !lang lang ***(Path: `csgo/addons/counterstrikesharp/plugins/CallAdmin/lang`)***
```
{
  "Prefix": "[{green}CallAdmin{default}]",
  "MissingCommandPermission": "{red}You don't have permission to use this command!",
  "NoPlayersAvailable": "There are no players available",
  "InCoolDown": "You are on a cooldown...wait {0} seconds and try again",
  "ReportSent": "Your report has been sent to the admins!",
  "WebhookError": "There was an error sending the webhook",
  "InsertIntoDatabaseError": "There was an error while inserting into database!",
  "ReportNotFound": "I couldn't find this report",
  "MarkedAsHandledButNotInDatabase": "This report has been marked as handled on Discord but not in database!",
  "ReportMarkedAsHandled": "This report has been marked as {green}handled!",
  "CustomReason": "Type the reason for the report",
  "Embed.Title": "Report",
  "Embed.Player": "Player",
  "Embed.PlayerName": "Name",
  "Embed.PlayerSteamid": "SteamID",
  "Embed.Suspect": "Suspect",
  "Embed.SuspectName": "Name",
  "Embed.SuspectSteamid": "SteamID",
  "Embed.Admin": "Admin",
  "Embed.AdminName": "Name",
  "Embed.AdminSteamid": "SteamID",
  "Embed.Reason": "Reason",
  "Embed.Ip": "Ip",
  "Embed.Map": "Map",
  "Embed.Content": "**!{0} {1}** in the game to mark this report as handled. -> You can write anything here or leave it blank. Ping a member like this: <@MemberId> or a role: <@&RoleId>",
  "ChatMenu.ReasonsTitle": "[{green}REPORT{default}] Choose a Reason",
  "ChatMenu.PlayersTitle": "[{green}REPORT{default}] Choose a Player"
}
```
