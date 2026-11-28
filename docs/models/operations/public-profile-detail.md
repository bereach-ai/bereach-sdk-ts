# PublicProfileDetail

How much of each person to read. "preview" (default for one profile): a quick look; it can miss the current title and older posts. "full" (default for several): every detail we have. Choose full for one person when the job title, how long they have held it, or the whole dated career matters. On full, a person a search already returned is answered from that search's record.

## Example Usage

```typescript
import { PublicProfileDetail } from "bereach/models/operations";

let value: PublicProfileDetail = "full";
```

## Values

```typescript
"preview" | "full"
```