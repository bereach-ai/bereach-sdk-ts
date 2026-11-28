# PublicFindPeopleRefused

Set when the request could not be answered. 'nothing-to-search' means nothing in it named anybody. 'wants-companies' means it asked for organisations, which this operation does not find: use the company search instead. 'off-topic' means the index answered about a different subject, so nobody it returned was shown: that is a market this search could not reach, never an empty market. 'wants-a-plan' means an agent asked for a crowd described by role, kind of company or place, which is a plan of searches (plan-searches), not this lookup; planNote says so. None of the four is a retry, say what happened and change the request.

## Example Usage

```typescript
import { PublicFindPeopleRefused } from "bereach/models/operations";

let value: PublicFindPeopleRefused = "off-topic";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"nothing-to-search" | "wants-companies" | "off-topic" | "wants-a-plan" | Unrecognized<string>
```