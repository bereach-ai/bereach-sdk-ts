# ContactsAddRequestBody

## Example Usage

```typescript
import { ContactsAddRequestBody } from "bereach/models/operations";

let value: ContactsAddRequestBody = {
  contacts: [],
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `contacts`                                                                         | [operations.ContactsAddContact](../../models/operations/contacts-add-contact.md)[] | :heavy_check_mark:                                                                 | Contacts to add (single or bulk)                                                   |