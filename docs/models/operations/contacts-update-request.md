# ContactsUpdateRequest

## Example Usage

```typescript
import { ContactsUpdateRequest } from "bereach/models/operations";

let value: ContactsUpdateRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                                                                 | Type                                                                                                                  | Required                                                                                                              | Description                                                                                                           |
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `campaignId`                                                                                                          | *string*                                                                                                              | :heavy_minus_sign:                                                                                                    | Scopes the write to one list. Required with lifecycleStage: take it from the person's campaigns in a contacts result. |
| `id`                                                                                                                  | *string*                                                                                                              | :heavy_check_mark:                                                                                                    | Contact ID                                                                                                            |
| `body`                                                                                                                | [operations.ContactsUpdateRequestBody](../../models/operations/contacts-update-request-body.md)                       | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |