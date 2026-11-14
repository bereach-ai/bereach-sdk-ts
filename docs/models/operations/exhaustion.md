# Exhaustion

Finer than moreAvailable: 'axes-exhausted' means every search angle for this audience has genuinely been tried, calling again with more will not find anybody new. 'batch-failed' means this attempt could not run, worth retrying. 'more-available' is the ordinary case.

## Example Usage

```typescript
import { Exhaustion } from "bereach/models/operations";

let value: Exhaustion = "axes-exhausted";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"more-available" | "axes-exhausted" | "batch-failed" | Unrecognized<string>
```