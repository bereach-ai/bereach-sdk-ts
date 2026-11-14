# FindEmailsStatus

found: found now, charged. already_saved: the email was already on the contact, free. already_found: found earlier for this person, who is not saved, free. not_found: no email returned, free; reason says why. not_looked_up: nothing left to spend, free. unavailable: could not be looked up now, free. unknown_contact: no saved person has this contact id, free. excluded: on this account's exclusion list, never looked up, free.

## Example Usage

```typescript
import { FindEmailsStatus } from "bereach/models/operations";

let value: FindEmailsStatus = "already_saved";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"found" | "already_saved" | "already_found" | "not_found" | "not_looked_up" | "unavailable" | "unknown_contact" | "excluded" | Unrecognized<string>
```