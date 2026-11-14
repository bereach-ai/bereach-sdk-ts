# InboxListSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { InboxListSpent } from "bereach/models/operations";

let value: InboxListSpent = {
  amount: 3435.44,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `amount`                                                                       | *number*                                                                       | :heavy_check_mark:                                                             | The money spent.                                                               |
| `currency`                                                                     | [operations.InboxListCurrency](../../models/operations/inbox-list-currency.md) | :heavy_check_mark:                                                             | N/A                                                                            |
| `text`                                                                         | *string*                                                                       | :heavy_check_mark:                                                             | The amount as a person reads it, with its currency.                            |