# FindPhonesReason

On a not_found row, why no number was returned. no_identity: nothing to look the person up by. nobody_has_it: no number was found. unreadable_number: the number found is not a valid number in any country. null on every other row.

## Example Usage

```typescript
import { FindPhonesReason } from "bereach/models/operations";

let value: FindPhonesReason = "nobody_has_it";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"no_identity" | "nobody_has_it" | "unreadable_number" | Unrecognized<string>
```