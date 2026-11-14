# ContactsBriefResponse

The brief

## Example Usage

```typescript
import { ContactsBriefResponse } from "bereach/models/operations";

let value: ContactsBriefResponse = {
  success: true,
  person: {
    found: true,
    contactId: "<id>",
    profileUrl: null,
    profile: {},
    standing: {
      outreachStatus: "<value>",
      invitedAt: "<value>",
      connectedAt: "<value>",
      lastContactedAt: "<value>",
      lastRepliedAt: null,
      doNotContact: false,
      lists: [],
    },
  },
  posts: {
    found: true,
    items: [],
  },
  activity: {
    found: true,
    lastReactionAt: "<value>",
    lastCommentAt: "<value>",
    reactions: [],
    comments: [],
  },
  company: {
    found: true,
    card: {
      readAt: "<value>",
      name: "<value>",
      slug: "<value>",
      url: "https://strict-linseed.biz",
      tagline: "<value>",
      description: "edge meh litter deceivingly whirlwind since",
      website: "<value>",
      industry: "<value>",
      founded: 7040.92,
      employees: 3517.73,
      followers: 4710.7,
      location: "<value>",
      recentPosts: [],
    },
  },
  signals: [],
  history: {
    found: false,
    readFrom: "account",
    verbatim: [],
    summary: {
      days: [],
      weeks: [
        {
          start: "<value>",
          end: "<value>",
          messages: 962975,
          summary: "<value>",
        },
      ],
      months: [],
      waiting: 739286,
    },
    totalMessages: 15906,
    oldestAt: "<value>",
    complete: false,
  },
  readAt: "<value>",
  creditsUsed: 354,
  retryAfter: 731902,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `person`                                                                                                                             | [operations.ContactsBriefPerson](../../models/operations/contacts-brief-person.md)                                                   | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `posts`                                                                                                                              | [operations.Posts](../../models/operations/posts.md)                                                                                 | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `activity`                                                                                                                           | [operations.ContactsBriefActivity](../../models/operations/contacts-brief-activity.md)                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `company`                                                                                                                            | [operations.ContactsBriefCompany](../../models/operations/contacts-brief-company.md)                                                 | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `signals`                                                                                                                            | [operations.Signal](../../models/operations/signal.md)[]                                                                             | :heavy_check_mark:                                                                                                                   | Dated reasons to write now, newest first, each with a link to check it.                                                              |
| `signalsReason`                                                                                                                      | [operations.SignalsReason](../../models/operations/signals-reason.md)                                                                | :heavy_minus_sign:                                                                                                                   | Why this part is empty or older than asked.                                                                                          |
| `history`                                                                                                                            | [operations.History](../../models/operations/history.md)                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `readAt`                                                                                                                             | *string*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ContactsBriefSpent](../../models/operations/contacts-brief-spent.md)                                                     | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |