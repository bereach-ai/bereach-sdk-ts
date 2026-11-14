# PublicProfileReadFrom

Where a profile read in full was read: the record a search of yours already saved, or a public record read today.

## Example Usage

```typescript
import { PublicProfileReadFrom } from "bereach/models/operations";

let value: PublicProfileReadFrom = "search";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"search" | "records" | Unrecognized<string>
```