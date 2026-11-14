# ScheduledMessageListConnection

Where this account stands with them, which decides what approving does: connected means the message goes in line, invited means it waits for an acceptance, not_connected means a connection request goes out first. Null on a connection request row.

## Example Usage

```typescript
import { ScheduledMessageListConnection } from "bereach/models/operations";

let value: ScheduledMessageListConnection = "invited";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"connected" | "invited" | "not_connected" | Unrecognized<string>
```