# MessageStatus

The row's own status. `scheduled` is legacy, read as `draft` (see `firstDm`).

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