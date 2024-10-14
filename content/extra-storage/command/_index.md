+++
title = "Commands & Permissions"
weight = 2
+++

## These commands for players:

| Player Command | Permission | Description |
| --- | --- | --- |
| /exstorage help | `exstorage.command.player.help` | Players can see help page. |
| /exstorage \[player\] | `exstorage.command.player.open` | Players can open their storage, or open another player's storage. |
| /exstorage toggle | `exstorage.command.player.toggle` | Players can turn on / off the feature if they don't want to use. |
| /exstorage filter | `exstorage.command.player.filter` | Players can open their filter. |
| /exstorage partner \[add/remove/clear\]\[player\] | `exstorage.command.player.partner` | Players can use the partner feature. Or open a GUI to see who was their partners. |
| /exstorage sell \[%material-key% \[amount\]\] | `exstorage.command.player.sell` | Players can open the market to sell items that contain in their storage. |
| /exstorage withdraw %material-key% \[amount\] | `exstorage.command.player.withdraw` | Withdraw items without opening the GUI. |

## These commands for administrator only:

| Admin Command | Permission | Description |
| --- | --- | --- |
|     | `exstorage.*` | The highest permission. |
| /esadmin open %player% | `exstorage.command.admin.open` | Open and use another player's storage without any conditions. |
| **/esadmin space %amount% \[player/\*\]  <br>/esadmin addspace %amount% \[player/\*\]** | `exstorage.command.admin.space` | Change the maximum space of the player's storage (\* for all of players). |
| /esadmin add %material-key% %amount% \[player\] | `exstorage.command.admin.add` | Allows the player to add item quantity to the storage. |
| /esadmin subtract %material-key% %amount% \[player\] | `exstorage.command.admin.subtract` | Allows the player to subtract item quantity to the storage. |
| /esadmin set %material-key% %amount% \[player\] | `exstorage.command.admin.set` | Allows the player to set their item quantity in the storage. |
| /exstorage withdraw %material-key% \[amount\] | `exstorage.command.player.withdraw` | Withdraw items without opening the GUI. |
| /esadmin whitelist | `exstorage.command.admin.whitelist` | Modify the "Whitelist" section in config.yml in-game. Apply changes immediately when adding/removing an item. |
| /esadmin reload | `exstorage.command.admin.reload` | Reload the configurations. |
