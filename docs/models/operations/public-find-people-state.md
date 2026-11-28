# PublicFindPeopleState

found; nobody-holds-role: people work there, none in a role asked; nobody-there: the company could not be found; nobody-in-place: none in the place asked; not-reached: not searched yet, asking again with more continues; failed: could not be searched just now, asking again with more retries it.

## Example Usage

```typescript
import { PublicFindPeopleState } from "bereach/models/operations";

let value: PublicFindPeopleState = "failed";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"found" | "nobody-holds-role" | "nobody-there" | "nobody-in-place" | "not-reached" | "failed" | Unrecognized<string>
```