# BlockedKind

Why nothing is going out. The ordinary spacing between two invitations is state 'spacing', never a block.

## Example Usage

```typescript
import { BlockedKind } from "bereach/models/operations";

let value: BlockedKind = "challenge";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"challenge" | "session_dead" | "no_plan" | "resting" | "invite_cap" | "warming_up" | "rate_limited" | Unrecognized<string>
```