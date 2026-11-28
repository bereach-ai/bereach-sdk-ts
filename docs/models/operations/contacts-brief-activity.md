# ContactsBriefActivity

## Example Usage

```typescript
import { ContactsBriefActivity } from "bereach/models/operations";

let value: ContactsBriefActivity = {
  found: false,
  lastReactionAt: "<value>",
  lastCommentAt: "<value>",
  reactions: [],
  comments: [
    {
      at: "<value>",
      text: "<value>",
      postUrl: "https://ruddy-icebreaker.name",
      postAuthor: "<value>",
    },
  ],
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `found`                                                                      | *boolean*                                                                    | :heavy_check_mark:                                                           | N/A                                                                          |
| `reason`                                                                     | [operations.ActivityReason](../../models/operations/activity-reason.md)      | :heavy_minus_sign:                                                           | Why this part is empty or older than asked.                                  |
| `readFrom`                                                                   | [operations.ActivityReadFrom](../../models/operations/activity-read-from.md) | :heavy_minus_sign:                                                           | N/A                                                                          |
| `readAt`                                                                     | *string*                                                                     | :heavy_minus_sign:                                                           | When what this part shows was read.                                          |
| `lastReactionAt`                                                             | *string*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `lastCommentAt`                                                              | *string*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `reactions`                                                                  | [operations.Reaction](../../models/operations/reaction.md)[]                 | :heavy_check_mark:                                                           | N/A                                                                          |
| `comments`                                                                   | [operations.Comment](../../models/operations/comment.md)[]                   | :heavy_check_mark:                                                           | N/A                                                                          |