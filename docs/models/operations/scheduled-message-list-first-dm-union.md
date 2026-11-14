# ScheduledMessageListFirstDmUnion

Where this person's first message stands, from the one projection every surface reads. Present on list rows.


## Supported Types

### `operations.ScheduledMessageListFirstDmNone`

```typescript
const value: operations.ScheduledMessageListFirstDmNone = {
  kind: "none",
};
```

### `operations.ScheduledMessageListFirstDmWritten`

```typescript
const value: operations.ScheduledMessageListFirstDmWritten = {
  kind: "written",
  scheduledMessageId: "<id>",
};
```

### `operations.ScheduledMessageListFirstDmHeld`

```typescript
const value: operations.ScheduledMessageListFirstDmHeld = {
  kind: "held",
  scheduledMessageId: "<id>",
  reason: "<value>",
};
```

### `operations.ScheduledMessageListFirstDmQueued`

```typescript
const value: operations.ScheduledMessageListFirstDmQueued = {
  kind: "queued",
  scheduledMessageId: "<id>",
  why: {
    status: "not-on-list",
    detail: "<value>",
    position: 631546,
    opensAt: "<value>",
    clearsItself: true,
    fixUrl: "https://jealous-collectivization.info/",
    kind: "<value>",
  },
};
```

### `operations.ScheduledMessageListFirstDmSending`

```typescript
const value: operations.ScheduledMessageListFirstDmSending = {
  kind: "sending",
  scheduledMessageId: "<id>",
};
```

### `operations.ScheduledMessageListFirstDmSent`

```typescript
const value: operations.ScheduledMessageListFirstDmSent = {
  kind: "sent",
  scheduledMessageId: "<id>",
  sentAt: "<value>",
};
```

### `operations.ScheduledMessageListFirstDmFailed`

```typescript
const value: operations.ScheduledMessageListFirstDmFailed = {
  kind: "failed",
  scheduledMessageId: "<id>",
  reason: "<value>",
  canRequeue: true,
};
```

### `operations.ScheduledMessageListFirstDmCancelled`

```typescript
const value: operations.ScheduledMessageListFirstDmCancelled = {
  kind: "cancelled",
  scheduledMessageId: "<id>",
  reason: "<value>",
};
```

