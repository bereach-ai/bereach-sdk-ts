# PublicFindPeopleNotAppliedReason

Why it was taken out: it came from the saved target rather than the ask, or the request did not ask for it.

## Example Usage

```typescript
import { PublicFindPeopleNotAppliedReason } from "bereach/models/operations";

let value: PublicFindPeopleNotAppliedReason = "not-asked";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"saved-target" | "not-asked" | Unrecognized<string>
```