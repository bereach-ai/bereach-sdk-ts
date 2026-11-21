# HistoryReason

Why the conversation was not read anew from the account. rate_limited: too many conversations were asked for at the same moment, so the messages already held are shown; ask for this person again on their own. It never limits sending messages.

## Example Usage

```typescript
import { HistoryReason } from "bereach/models/operations";

let value: HistoryReason = "trial_limit";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"not_asked" | "not_found" | "no_person" | "no_company" | "unavailable" | "credits" | "usage_limit" | "trial_limit" | "no_account" | "account_signed_out" | "account_settling" | "no_member_id" | "no_conversation" | "unreadable" | "rate_limited" | "no_contact" | Unrecognized<string>
```