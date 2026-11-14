# FindConversationSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { FindConversationSpent } from "bereach/models/operations";

let value: FindConversationSpent = {
  amount: 8835.46,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `amount`                                                                                     | *number*                                                                                     | :heavy_check_mark:                                                                           | The money spent.                                                                             |
| `currency`                                                                                   | [operations.FindConversationCurrency](../../models/operations/find-conversation-currency.md) | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `text`                                                                                       | *string*                                                                                     | :heavy_check_mark:                                                                           | The amount as a person reads it, with its currency.                                          |