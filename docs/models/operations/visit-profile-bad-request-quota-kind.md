# VisitProfileBadRequestQuotaKind

On a 429, what was refused. credits: a budget refused the call, error.details says which (the five-hour usage limit, the trial's included usage, or nothing left to spend).

## Example Usage

```typescript
import { VisitProfileBadRequestQuotaKind } from "bereach/models/operations";

let value: VisitProfileBadRequestQuotaKind = "ai-model-rate";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"credits" | "daily-cap" | "linkedin-rate" | "ai-model-rate" | "pacing" | Unrecognized<string>
```