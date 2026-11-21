# Standing

Where they stand with the user: invited, connected, messaged, replied, and the lists they are on.

## Example Usage

```typescript
import { Standing } from "bereach/models/operations";

let value: Standing = {
  outreachStatus: "<value>",
  invitedAt: "<value>",
  connectedAt: "<value>",
  lastContactedAt: "<value>",
  lastRepliedAt: "<value>",
  doNotContact: true,
  lists: [],
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `outreachStatus`                                                                 | *string*                                                                         | :heavy_check_mark:                                                               | N/A                                                                              |
| `invitedAt`                                                                      | *string*                                                                         | :heavy_check_mark:                                                               | N/A                                                                              |
| `connectedAt`                                                                    | *string*                                                                         | :heavy_check_mark:                                                               | N/A                                                                              |
| `lastContactedAt`                                                                | *string*                                                                         | :heavy_check_mark:                                                               | N/A                                                                              |
| `lastRepliedAt`                                                                  | *string*                                                                         | :heavy_check_mark:                                                               | N/A                                                                              |
| `doNotContact`                                                                   | *boolean*                                                                        | :heavy_check_mark:                                                               | N/A                                                                              |
| `lists`                                                                          | [operations.ContactsBriefList](../../models/operations/contacts-brief-list.md)[] | :heavy_check_mark:                                                               | N/A                                                                              |