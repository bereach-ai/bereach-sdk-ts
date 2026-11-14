# UpcomingStatus

next is first in line, not sent; waiting names the place; window means the account's sending hours are shut and opensAt says when they start again; blocked means the account is stopped.

## Example Usage

```typescript
import { UpcomingStatus } from "bereach/models/operations";

let value: UpcomingStatus = "next";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"next" | "waiting" | "window" | "blocked" | "not-on-list" | Unrecognized<string>
```