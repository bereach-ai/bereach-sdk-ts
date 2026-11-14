# ContactsUpsertRequest

## Example Usage

```typescript
import { ContactsUpsertRequest } from "bereach/models/operations";

let value: ContactsUpsertRequest = {
  contacts: [],
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `contacts`                                                                                              | [operations.ContactsUpsertContactRequest](../../models/operations/contacts-upsert-contact-request.md)[] | :heavy_check_mark:                                                                                      | Contacts to add (single or bulk)                                                                        |