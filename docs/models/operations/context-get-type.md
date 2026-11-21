# ContextGetType

## Example Usage

```typescript
import { ContextGetType } from "bereach/models/operations";

let value: ContextGetType = "credential:linkedin_long_broken";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"reply:received" | "connection:accepted" | "campaign:rate_limited" | "campaign:linkedin_expired" | "credential:llm_error" | "credential:linkedin_long_broken" | Unrecognized<string>
```