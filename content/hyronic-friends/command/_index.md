+++
title = "Commands & Permissions"
weight = 3
+++

## Permissions

### General permissions

| Permissions | Default | Description |
| --- | --- | --- |
| `hyronicfriends.*` | FALSE | `Allows the player to access everything of the plugin.` |
| `hyronicfriends.mails.size.maximum` | OP  | `Allows the player to have the maximum number of attached item slots.` |
| `hyronicfriends.friends.size.unlimited` | OP  | `Allows the player to have an unlimited list of friends.` |

### Command permissions

| Permissions | Default | Description |
| --- | --- | --- |
| `hyronicfriends.command.*` | FALSE | `Allows the player to access all commands of the plugin.` |
| `hyronicfriends.command.help` | OP  | `Allows the player to view the help page command.` |
| `hyronicfriends.command.friends` | OP  | `Allows the player to manage their friend list.` |
| `hyronicfriends.command.block` | OP  | `Allows the player to block (or unblock) a player.` |
| `hyronicfriends.command.teleport` | OP  | `Allows the player to teleport to their friends.` |
| `hyronicfriends.command.mail` | OP  | `Allows the player to send (or read) mail to their friends.` |
| `hyronicfriends.command.reload` | OP  | `Allows the player to reload the configuration.` |

## Commands

> [!CAUTION]
> We provide you with many commands. Some of them have been shortened, so we'll split them up into different tables.

### General commands

| Commands | Description |
| --- | --- |
| `/friend help [page]` | `View the help page command` |
| `/friend` | `Open main menu` |
| `/friend toggle` | `Toggle receive friend request` |
| `/friend notify` | `Turn on/off your friend online status` |
| `/friend add <player>` | `Send a friend request` |
| `/friend accept <player>` | `Accept a friend request` |
| `/friend decline <player>` | `Decline a friend request` |
| `/friend cancel <player>` | `Cancel the sent friend request` |
| `/friend list` | `Open your friend list` |
| `/friend reload` | `Reload the configuration` |
| `/unfriend <player>` | `Unfriend a player` |

### Blocking commands

| Commands | Description |
| --- | --- |
| `/blockedlist` | `Open your blocked list` |
| `/block <player>` | `Block a player` |
| `/unblock <player>` | `Unblock a player` |

### Teleport commands

| Commands | Description |
| --- | --- |
| `/ftp <player>` | `Teleport to your friend` |
| `/toggletp <player>` | `Allow/Disallow your friend to teleport to you` |

### Private message commands

| Commands | Description |
| --- | --- |
| `/togglemsg <player>` | `Enable/Disable receiving your friend message` |
| `/fmsg <player> <message>` | `Send private message to your friend` |
| `/freply <message>` | `Quick reply to the most recent message` |

### Mail commands

| Commands | Description |
| --- | --- |
| `/mail help` | `View the list of mail commands` |
| `/mailbox` | `Open your mailbox` |
| `/mail <player>` | `See all mails sent/received to/from a player` |
| `/mail send <player> <content>` | `Send mail to your friend` |
| `/mail read <player>` | `Read the recently received mail` |
| `/togglemail <player>` | `Allow/Disallow your friend to send mail to you` |
