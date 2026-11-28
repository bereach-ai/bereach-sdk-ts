# DiscardContactsRequest

## Example Usage

```typescript
import { DiscardContactsRequest } from "bereach/models/operations";

let value: DiscardContactsRequest = {
  body: {
    contactIds: [
      "<value 1>",
    ],
    update: {},
  },
};
```

## Fields

| Field                                                                                                                                                                                             | Type                                                                                                                                                                                              | Required                                                                                                                                                                                          | Description                                                                                                                                                                                       |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `campaignId`                                                                                                                                                                                      | *string*                                                                                                                                                                                          | :heavy_minus_sign:                                                                                                                                                                                | The list a list change (lifecycleStage) lands on: take it from the person's campaigns in a contacts result. Inside a conversation that has its own list, that list is used when this is left out. |
| `body`                                                                                                                                                                                            | [operations.DiscardContactsRequestBody](../../models/operations/discard-contacts-request-body.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                                                | N/A                                                                                                                                                                                               |