# Posts

## Example Usage

```typescript
import { Posts } from "bereach/models/operations";

let value: Posts = {
  found: true,
  items: [],
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `found`                                                                          | *boolean*                                                                        | :heavy_check_mark:                                                               | N/A                                                                              |
| `reason`                                                                         | [operations.PostsReason](../../models/operations/posts-reason.md)                | :heavy_minus_sign:                                                               | Why this part is empty or older than asked.                                      |
| `readFrom`                                                                       | [operations.PostsReadFrom](../../models/operations/posts-read-from.md)           | :heavy_minus_sign:                                                               | N/A                                                                              |
| `readAt`                                                                         | *string*                                                                         | :heavy_minus_sign:                                                               | When what this part shows was read.                                              |
| `items`                                                                          | [operations.ContactsBriefItem](../../models/operations/contacts-brief-item.md)[] | :heavy_check_mark:                                                               | N/A                                                                              |