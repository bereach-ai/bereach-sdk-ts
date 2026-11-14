# CompanyOnProfile

Whether their own profile names the company now, before, or not yet: a profile can lag the news by weeks.

## Example Usage

```typescript
import { CompanyOnProfile } from "bereach/models/operations";

let value: CompanyOnProfile = "no";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"now" | "before" | "no" | Unrecognized<string>
```