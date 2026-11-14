# AuthorKind

Whether a person or a company page published the post, read off their own page. Null when neither page was found.

## Example Usage

```typescript
import { AuthorKind } from "bereach/models/operations";

let value: AuthorKind = "company";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"person" | "company" | Unrecognized<string>
```