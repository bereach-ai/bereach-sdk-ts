# EmployerUnread

Why this person carries no employer facts.

## Example Usage

```typescript
import { EmployerUnread } from "bereach/models/operations";

let value: EmployerUnread = "no company record";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"no current employer on the profile" | "no company record" | "could not be checked just now; running the plan again checks it" | "not checked in this run" | Unrecognized<string>
```