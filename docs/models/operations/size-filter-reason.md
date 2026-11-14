# SizeFilterReason

Why it was not applied: the search names its answer, the size came from the saved target rather than the ask, or the request did not ask for it.

## Example Usage

```typescript
import { SizeFilterReason } from "bereach/models/operations";

let value: SizeFilterReason = "named-company";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"named-company" | "saved-target" | "not-asked" | Unrecognized<string>
```