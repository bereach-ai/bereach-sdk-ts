# ContactsListRequest

## Example Usage

```typescript
import { ContactsListRequest } from "bereach/models/operations";

let value: ContactsListRequest = {
  campaignId: "<id>",
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `lifecycleStage`                                                                                  | [operations.ContactsListLifecycleStage](../../models/operations/contacts-list-lifecycle-stage.md) | :heavy_minus_sign:                                                                                | N/A                                                                                               |
| `source`                                                                                          | *string*                                                                                          | :heavy_minus_sign:                                                                                | N/A                                                                                               |
| `sourceAngle`                                                                                     | *string*                                                                                          | :heavy_minus_sign:                                                                                | N/A                                                                                               |
| `limit`                                                                                           | *number*                                                                                          | :heavy_minus_sign:                                                                                | N/A                                                                                               |
| `offset`                                                                                          | *number*                                                                                          | :heavy_minus_sign:                                                                                | N/A                                                                                               |
| `campaignId`                                                                                      | *string*                                                                                          | :heavy_check_mark:                                                                                | Campaign ID                                                                                       |