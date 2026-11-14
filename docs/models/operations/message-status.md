# MessageStatus

The row's own status. For a first message, `scheduled` is legacy, read as `draft` (see `firstDm`); for a connection request, `scheduled` means approved and in the invitation queue.

## Example Usage

```typescript
import { MessageStatus } from "bereach/models/operations";

let value: MessageStatus = "failed";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"draft" | "scheduled" | "sending" | "sent" | "failed" | "cancelled" | Unrecognized<string>
```