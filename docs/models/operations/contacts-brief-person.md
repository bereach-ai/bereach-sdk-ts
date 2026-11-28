# ContactsBriefPerson

## Example Usage

```typescript
import { ContactsBriefPerson } from "bereach/models/operations";

let value: ContactsBriefPerson = {
  found: true,
  contactId: null,
  profileUrl: "https://posh-hammock.net/",
  profile: {
    "key": "<value>",
    "key1": "<value>",
  },
  standing: {
    outreachStatus: "<value>",
    invitedAt: "<value>",
    connectedAt: "<value>",
    lastContactedAt: "<value>",
    lastRepliedAt: null,
    doNotContact: false,
    lists: [],
  },
};
```

## Fields

| Field                                                                                                                                                                         | Type                                                                                                                                                                          | Required                                                                                                                                                                      | Description                                                                                                                                                                   |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `found`                                                                                                                                                                       | *boolean*                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                            | N/A                                                                                                                                                                           |
| `reason`                                                                                                                                                                      | [operations.ContactsBriefPersonReason](../../models/operations/contacts-brief-person-reason.md)                                                                               | :heavy_minus_sign:                                                                                                                                                            | Why this part is empty or older than asked.                                                                                                                                   |
| `readFrom`                                                                                                                                                                    | [operations.PersonReadFrom](../../models/operations/person-read-from.md)                                                                                                      | :heavy_minus_sign:                                                                                                                                                            | N/A                                                                                                                                                                           |
| `readAt`                                                                                                                                                                      | *string*                                                                                                                                                                      | :heavy_minus_sign:                                                                                                                                                            | When what this part shows was read.                                                                                                                                           |
| `contactId`                                                                                                                                                                   | *string*                                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                            | N/A                                                                                                                                                                           |
| `profileUrl`                                                                                                                                                                  | *string*                                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                            | N/A                                                                                                                                                                           |
| `profile`                                                                                                                                                                     | Record<string, *any*>                                                                                                                                                         | :heavy_check_mark:                                                                                                                                                            | Who they are: name, headline, current title and company with start date, dated career, schools, About, languages, place, counts, skills and the statuses their profile shows. |
| `standing`                                                                                                                                                                    | [operations.Standing](../../models/operations/standing.md)                                                                                                                    | :heavy_check_mark:                                                                                                                                                            | Where they stand with the user: invited, connected, messaged, replied, and the lists they are on.                                                                             |