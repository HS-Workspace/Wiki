+++
title = "Developer APIs"
+++

## General player data

We provide you with a class named `/api/user/User.java` that gives you general player data, including the list of friends, the list of blocked players, mailbox, and more... You can use 2 methods provided from `public class FriendAPI` to get the player data:

``` java {title="/api/FriendAPI.java"}
Optional<User> FriendAPI.findUser(UUID);
Optional<User> FriendAPI.findUser(OfflinePlayer);
```

## List of friends

To get the list of all your friends:

``` java {title="/api/friend/FriendList.java"}
List<Friend> getList();
```

## List of online friends

To get the list of online friends:

``` java {title="/api/friend/FriendList.java"}
List<Friend> getOnlineFriends();
```

## List of blocked players

To get the list of blocked players:

``` java {title="/api/blocked/BlockedList.java"}
BlockedList getBlockedList();
```

## Blocking a player

To block a player you are hating:

``` java {title="/api/blocked/BlockedList.java"}
void block(UUID target);
```

## Unblocking a player

To unblock a player:

``` java {title="/api/blocked/BlockedList.java"}
void unblock(UUID target);
```

## Friend request

To send a friend request to a player:

``` java {title="/api/user/User.java"}
void sendRequest(UUID target);
```

## Find pending friend request

To find a friend request you received recently but are waiting for response:

``` java {title="/api/request/RequestList.java"}
Optional<Request> findWaitingRequest(UUID target, boolean checkExpire);
```

## Add new friend

To immediately add a player to your friend list:

``` java {title="/api/friend/FriendList.java"}
void addFriend(UUID target);
```

## Unfriend a player

To remove a player from your friend list:

``` java {title="/api/friend/FriendList.java"}
void unfriend(UUID target);
```

## Allow the player's friends to teleport to them

Before teleporting to your friend, you should check whether your friend allows you to teleport to them by using the method below:

``` java {title="/api/friend/Friend.java"}
boolean canTeleportTo();
```

To check whether your friend can teleport to you, use this method:

``` java {title="/api/friend/Friend.java"}
boolean canTeleport();
```

To allow/disallow your friend to teleport to you, use this method:

``` java {title="/api/friend/Friend.java"}
boolean setCanTeleport(boolean canTeleport);
```

## Allow to receive mail from friends

``` java {title="/api/friend/Friend.java"}
boolean canMail(); // Checks whether the player can receive the mail of their friend or not.
void setCanMail(boolean canMail); // Sets whether the player can receive the mail of their friend or not.
```

## Mailbox

This mailbox will contain all mails, including mails you have sent and mails you have received from your friends. It can be invoked from the `User` class:

``` java {title="/api/mail/Mailbox.java"}
Mailbox getMailbox();
```

## Send new mail

To send a mail to your friend:

``` java {title="/api/mail/Mail.java"}
Mail mail = new MailImpl(UUID sender, UUID target, String content, ItemStack... items);
mail.send();
```

## Attached items

To get attached items from a letter:

``` java {title="/api/mail/Mail.java"}
List<ItemStack> getAttachedItem();
```

## Sender - revoke items from mail

There are 2 methods that allow you to revoke your items from the letter:

``` java {title="/api/mail/Mail.java"}
boolean revokeItem(ItemStack item); // Revoke the specified item.
boolean revokeAllItems(); // Revoke all items contained in the letter.
```

## Receiver - take items from mail

Same as revoke items, there are 2 methods that allow you to take items from the letter:

``` java {title="/api/mail/Mail.java"}
boolean takeItem(ItemStack item); // Take the specified item.
boolean takeAllItems(); // Take all items contained in the letter.
```

## Events

We also provide you with some event classes, see details at: [**Events API**](./event).
