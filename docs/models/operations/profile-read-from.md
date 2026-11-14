# ProfileReadFrom

How fresh the profile is: from a search of yours (search; readAt says when), or read today (records, page).

## Example Usage

```typescript
import { ProfileReadFrom } from "bereach/models/operations";

let value: ProfileReadFrom = "search";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"search" | "records" | "page" | Unrecognized<string>
```