# PublicProfileOutcome

found: read. not_found: the address names no readable profile. unreadable: not read this time; asking again may reach it.

## Example Usage

```typescript
import { PublicProfileOutcome } from "bereach/models/operations";

let value: PublicProfileOutcome = "unreadable";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"found" | "not_found" | "unreadable" | Unrecognized<string>
```