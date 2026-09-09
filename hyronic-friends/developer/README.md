# Developer APIs

## General player data

We provide you with a class named `/api/user/User.java` that gives you general player data, including the list of friends, the list of blocked players, mailbox, and more... You can use 2 methods provided from `public class FriendAPI` to get the player data:

**File: `/api/FriendAPI.java`**
```java
Optional<User> FriendAPI.findUser(UUID);
Optional<User> FriendAPI.findUser(OfflinePlayer);
```

## List of friends

To get the list of all your friends:

**File: `/api/friend/FriendList.java`**
```java
List<Friend> getList();
```

## List of online friends

To get the list of online friends:

**File: `/api/friend/FriendList.java`**
```java
List<Friend> getOnlineFriends();
```

## List of blocked players

To get the list of blocked players:

**File: `/api/blocked/BlockedList.java`**
```java
BlockedList getBlockedList();
```

## Blocking a player

To block a player you are hating:

**File: `/api/blocked/BlockedList.java`**
```java
void block(UUID target);
```

## Unblocking a player

To unblock a player:

**File: `/api/blocked/BlockedList.java`**
```java
void unblock(UUID target);
```

## Friend request

To send a friend request to a player:

**File: `/api/user/User.java`**
```java
void sendRequest(UUID target);
```

## Find pending friend request

To find a friend request you received recently but are waiting for response:

**File: `/api/request/RequestList.java`**
```java
Optional<Request> findWaitingRequest(UUID target, boolean checkExpire);
```

## Add new friend

To immediately add a player to your friend list:

**File: `/api/friend/FriendList.java`**
```java
void addFriend(UUID target);
```

## Unfriend a player

To remove a player from your friend list:

**File: `/api/friend/FriendList.java`**
```java
void unfriend(UUID target);
```

## Allow the player's friends to teleport to them

Before teleporting to your friend, you should check whether your friend allows you to teleport to them by using the method below:

**File: `/api/friend/Friend.java`**
```java
boolean canTeleportTo();
```

To check whether your friend can teleport to you, use this method:

**File: `/api/friend/Friend.java`**
```java
boolean canTeleport();
```

To allow/disallow your friend to teleport to you, use this method:

**File: `/api/friend/Friend.java`**
```java
boolean setCanTeleport(boolean canTeleport);
```

## Allow to receive mail from friends

**File: `/api/friend/Friend.java`**
```java
boolean canMail(); // Checks whether the player can receive the mail of their friend or not.
void setCanMail(boolean canMail); // Sets whether the player can receive the mail of their friend or not.
```

## Mailbox

This mailbox will contain all mails, including mails you have sent and mails you have received from your friends. It can be invoked from the `User` class:

**File: `/api/mail/Mailbox.java`**
```java
Mailbox getMailbox();
```

## Send new mail

To send a mail to your friend:

**File: `/api/mail/Mail.java`**
```java
Mail mail = new MailImpl(UUID sender, UUID target, String content, ItemStack... items);
mail.send();
```

## Attached items

To get attached items from a letter:

**File: `/api/mail/Mail.java`**
```java
List<ItemStack> getAttachedItem();
```

## Sender - revoke items from mail

There are 2 methods that allow you to revoke your items from the letter:

**File: `/api/mail/Mail.java`**
```java
boolean revokeItem(ItemStack item); // Revoke the specified item.
boolean revokeAllItems(); // Revoke all items contained in the letter.
```

## Receiver - take items from mail

Same as revoke items, there are 2 methods that allow you to take items from the letter:

**File: `/api/mail/Mail.java`**
```java
boolean takeItem(ItemStack item); // Take the specified item.
boolean takeAllItems(); // Take all items contained in the letter.
```

## Events

We also provide you with some event classes, see details at: [**Events API**](./event/).
