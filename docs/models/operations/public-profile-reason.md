# PublicProfileReason

Why an unreadable row was not read.

## Example Usage

```typescript
import { PublicProfileReason } from "bereach/models/operations";

let value: PublicProfileReason = "timed_out";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"rate_limited" | "credits" | "usage_limit" | "trial_limit" | "timed_out" | "failed" | Unrecognized<string>
```