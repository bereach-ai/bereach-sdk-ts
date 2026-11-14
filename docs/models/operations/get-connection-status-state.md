# GetConnectionStatusState

What the account is doing. nothing_queued: nobody is waiting. sending: invitations are going out. spacing: between two invitations, a matter of minutes. waiting_for_window: people are waiting and this account only sends during its own set hours, so the next one goes at nextSendAt, which can be hours away and is not a fault. blocked: something is stopping it, and blocked says what.

## Example Usage

```typescript
import { GetConnectionStatusState } from "bereach/models/operations";

let value: GetConnectionStatusState = "blocked";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"nothing_queued" | "sending" | "spacing" | "waiting_for_window" | "blocked" | Unrecognized<string>
```