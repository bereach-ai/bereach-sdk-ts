# AuthorPageMissing

Why authorUrl is null: no public page holds the post's handle, the read of who wrote it failed, the page found carries another name than the post shows, or the handle is both a person and a company page and the post shows no name to tell them apart.

## Example Usage

```typescript
import { AuthorPageMissing } from "bereach/models/operations";

let value: AuthorPageMissing = "no_public_page";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"no_public_page" | "read_failed" | "name_differs" | "person_or_company_unclear" | Unrecognized<string>
```