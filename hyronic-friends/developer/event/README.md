# Events

## PreFriendRequestSendEvent

Called before a friend request is sent

**File: `/api/events/PreFriendRequestSendEvent.java`**
```java
public final class PreFriendRequestSendEvent extends BaseEvent implements Cancellable {
    private final Request request;
    private boolean cancelled;

    public PreFriendRequestSendEvent(Request request) {
        this.request = request;
        this.cancelled = false;
    }

    public Request getRequest() {
        return request;
    }

    @Override
    public boolean isCancelled() {
        return cancelled;
    }

    @Override
    public void setCancelled(boolean cancel) {
        this.cancelled = cancel;
    }
}
```

## PreFriendRequestRespondEvent

Called when a friend request is ready to respond (accept/decline/cancel)

**File: `/api/events/PreFriendRequestRespondEvent.java`**
```java
public final class PreFriendRequestRespondEvent extends BaseEvent implements Cancellable {
    private final Request request;
    private Request.Status status;
    private boolean cancelled;

    public PreFriendRequestRespondEvent(Request request, Request.Status status) {
        this.request = request;
        this.status = status;
        this.cancelled = false;
    }

    public Request getRequest() {
        return request;
    }

    public Request.Status getStatus() {
        return status;
    }

    public void setStatus(Request.Status status) {
        this.status = status;
    }

    @Override
    public boolean isCancelled() {
        return cancelled;
    }

    @Override
    public void setCancelled(boolean cancel) {
        this.cancelled = cancel;
    }
}
```

## FriendTeleportEvent

Called before your friend teleports to you

**File: `/api/events/FriendTeleportEvent.java`**
```java
public final class FriendTeleportEvent extends BaseEvent implements Cancellable {
    private final User user, target;
    private boolean cancelled;

    public FriendTeleportEvent(User user, User target) {
        this.user = user;
        this.target = target;
        this.cancelled = false;
    }

    public User getUser() {
        return user;
    }

    public User getTarget() {
        return target;
    }

    @Override
    public boolean isCancelled() {
        return cancelled;
    }

    @Override
    public void setCancelled(boolean cancel) {
        this.cancelled = cancel;
    }
}
```

## AttachingItemToMailEvent

Called before attaching items to your mail

**File: `/api/events/AttachingItemToMailEvent.java`**
```java
public final class AttachingItemToMailEvent extends BaseEvent implements Cancellable {
    private ItemStack item;
    private boolean cancelled;

    public AttachingItemToMailEvent(ItemStack item) {
        this.item = item;
        this.cancelled = false;
    }

    public ItemStack getAttachedItem() {
        return item;
    }

    public void setAttachedItem(ItemStack item) {
        this.item = item;
    }

    @Override
    public boolean isCancelled() {
        return cancelled;
    }

    @Override
    public void setCancelled(boolean cancel) {
        this.cancelled = cancel;
    }
}
```

## PreMailSendEvent

Called before your mail is sent

**File: `/api/events/PreMailSendEvent.java`**
```java
public final class PreMailSendEvent extends BaseEvent implements Cancellable {
    private final Mail mail;
    private boolean cancelled;

    public PreMailSendEvent(Mail mail) {
        this.mail = mail;
        this.cancelled = false;
    }

    public Mail getMail() {
        return mail;
    }

    @Override
    public boolean isCancelled() {
        return cancelled;
    }

    @Override
    public void setCancelled(boolean cancel) {
        this.cancelled = cancel;
    }
}
```

## PreMailRespondEvent

Called when a mail is ready to respond (read/cancel)

**File: `/api/events/PreMailRespondEvent.java`**
```java
public final class PreMailRespondEvent extends BaseEvent implements Cancellable {
    private final Mail mail;
    private Mail.Status status;
    private boolean cancelled;

    public PreMailRespondEvent(Mail mail, Mail.Status status) {
        this.mail = mail;
        this.status = status;
        this.cancelled = false;
    }

    public Mail getMail() {
        return mail;
    }

    public Mail.Status getStatus() {
        return status;
    }

    public void setStatus(Mail.Status status) {
        this.status = status;
    }

    @Override
    public boolean isCancelled() {
        return cancelled;
    }

    @Override
    public void setCancelled(boolean cancel) {
        this.cancelled = cancel;
    }
}
```
