# FindEmailsReason

On a not_found row, why no email was returned. no_identity: nothing to look the person up by. nobody_has_it: no address was found. provider_guess: only an unconfirmed guess was found. former_employer: the address found is at a company they left. dead_mailbox: the address found does not accept mail. unproven: the address found is on another domain or at a personal mail provider and nothing confirmed it. null on every other row.

## Example Usage

```typescript
import { FindEmailsReason } from "bereach/models/operations";

let value: FindEmailsReason = "nobody_has_it";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"no_identity" | "nobody_has_it" | "provider_guess" | "former_employer" | "dead_mailbox" | "unproven" | Unrecognized<string>
```