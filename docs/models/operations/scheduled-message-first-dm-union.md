# ScheduledMessageFirstDmUnion

Where this person's first message stands, from the one projection every surface reads. Present on list rows.


## Supported Types

### `operations.FirstDmScheduledMessageNone`

```typescript
const value: operations.FirstDmScheduledMessageNone = {
  kind: "none",
};
```

### `operations.FirstDmScheduledMessageWritten`

```typescript
const value: operations.FirstDmScheduledMessageWritten = {
  kind: "written",
  scheduledMessageId: "<id>",
};
```

### `operations.FirstDmScheduledMessageHeld`

```typescript
const value: operations.FirstDmScheduledMessageHeld = {
  kind: "held",
  scheduledMessageId: "<id>",
  reason: "<value>",
};
```

### `operations.FirstDmScheduledMessageQueued`

```typescript
const value: operations.FirstDmScheduledMessageQueued = {
  kind: "queued",
  scheduledMessageId: "<id>",
  why: {
    status: "accepted",
    detail: "<value>",
    position: 15508,
    opensAt: "<value>",
    clearsItself: false,
    fixUrl: "https://formal-annual.name",
    kind: "<value>",
  },
};
```

### `operations.FirstDmScheduledMessageSending`

```typescript
const value: operations.FirstDmScheduledMessageSending = {
  kind: "sending",
  scheduledMessageId: "<id>",
};
```

### `operations.FirstDmScheduledMessageSent`

```typescript
const value: operations.FirstDmScheduledMessageSent = {
  kind: "sent",
  scheduledMessageId: "<id>",
  sentAt: "<value>",
};
```

### `operations.FirstDmScheduledMessageFailed`

```typescript
const value: operations.FirstDmScheduledMessageFailed = {
  kind: "failed",
  scheduledMessageId: "<id>",
  reason: "<value>",
  canRequeue: true,
};
```

### `operations.FirstDmScheduledMessageCancelled`

```typescript
const value: operations.FirstDmScheduledMessageCancelled = {
  kind: "cancelled",
  scheduledMessageId: "<id>",
  reason: "<value>",
};
```

