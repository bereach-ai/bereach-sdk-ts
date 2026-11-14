# PublicEnrichDetail

How much of each person to read. "preview": a quick look; it can miss the current title and older posts. "full" (default): every detail we have. Keep full unless a quick look at each person is enough. A person a search already returned is not read again.

## Example Usage

```typescript
import { PublicEnrichDetail } from "bereach/models/operations";

let value: PublicEnrichDetail = "full";
```

## Values

```typescript
"preview" | "full"
```