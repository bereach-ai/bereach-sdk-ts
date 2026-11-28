# ScheduledMessageStatus

The row's own status. `scheduled` is legacy, read as `draft` (see `firstDm`).

## Example Usage

```typescript
import { ScheduledMessageStatus } from "bereach/models/operations";

let value: ScheduledMessageStatus = "cancelled";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"draft" | "scheduled" | "sending" | "sent" | "failed" | "cancelled" | Unrecognized<string>
```