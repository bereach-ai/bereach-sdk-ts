# ContactsListCampaignsSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { ContactsListCampaignsSpent } from "bereach/models/operations";

let value: ContactsListCampaignsSpent = {
  amount: 7352.48,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `amount`                                                                                                | *number*                                                                                                | :heavy_check_mark:                                                                                      | The money spent.                                                                                        |
| `currency`                                                                                              | [operations.ContactsListCampaignsCurrency](../../models/operations/contacts-list-campaigns-currency.md) | :heavy_check_mark:                                                                                      | N/A                                                                                                     |
| `text`                                                                                                  | *string*                                                                                                | :heavy_check_mark:                                                                                      | The amount as a person reads it, with its currency.                                                     |