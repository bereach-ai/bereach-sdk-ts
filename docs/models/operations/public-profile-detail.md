# PublicProfileDetail

How much of each person to read. "preview" (default for one profile): a quick look; it can miss the current title and older posts. "full" (default for several): every detail we have. Choose full for one person when the job title, how long they have held it, or the whole dated career matters. A person a search already returned is not read again.

## Example Usage

```typescript
import { PublicProfileDetail } from "bereach/models/operations";

let value: PublicProfileDetail = "full";
```

## Values

```typescript
"preview" | "full"
```