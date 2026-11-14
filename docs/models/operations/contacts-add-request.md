# ContactsAddRequest

## Example Usage

```typescript
import { ContactsAddRequest } from "bereach/models/operations";

let value: ContactsAddRequest = {
  campaignId: "<id>",
  body: {
    contacts: [
      {
        linkedinUrl: "https://bustling-underpants.name",
        name: "<value>",
      },
    ],
  },
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `campaignId`                                                                              | *string*                                                                                  | :heavy_check_mark:                                                                        | Campaign ID                                                                               |
| `body`                                                                                    | [operations.ContactsAddRequestBody](../../models/operations/contacts-add-request-body.md) | :heavy_check_mark:                                                                        | N/A                                                                                       |