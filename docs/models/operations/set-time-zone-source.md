# SetTimeZoneSource

Where the zone came from. setting: the user set it. none: nothing placed them, so the hours run on UTC. Any other value is an automatic guess, which the user can correct.

## Example Usage

```typescript
import { SetTimeZoneSource } from "bereach/models/operations";

let value: SetTimeZoneSource = "account";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"setting" | "browser" | "account" | "market" | "email" | "last_active" | "none" | Unrecognized<string>
```