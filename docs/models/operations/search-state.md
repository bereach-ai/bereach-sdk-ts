# SearchState

## Example Usage

```typescript
import { SearchState } from "bereach/models/operations";

let value: SearchState = "stopped";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"queued" | "searching" | "done" | "not_reachable" | "stopped" | "failed" | Unrecognized<string>
```