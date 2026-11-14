# PlacementRequest

Where these people join the queue. "front" is ahead of everyone already waiting; "end" is the ordinary place among them. Naming one person defaults to front, handing over several defaults to end. Say either explicitly to override that.

## Example Usage

```typescript
import { PlacementRequest } from "bereach/models/operations";

let value: PlacementRequest = "end";
```

## Values

```typescript
"front" | "end"
```