# ProgressState

## Example Usage

```typescript
import { ProgressState } from "bereach/models/operations";

let value: ProgressState = "done";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"running" | "done" | "stopped" | "failed" | Unrecognized<string>
```