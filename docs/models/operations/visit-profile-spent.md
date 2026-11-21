# VisitProfileSpent

What this call spent, in money.

## Example Usage

```typescript
import { VisitProfileSpent } from "bereach/models/operations";

let value: VisitProfileSpent = {
  amount: 9952.5,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `amount`                                                                             | *number*                                                                             | :heavy_check_mark:                                                                   | The money spent.                                                                     |
| `currency`                                                                           | [operations.VisitProfileCurrency](../../models/operations/visit-profile-currency.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `text`                                                                               | *string*                                                                             | :heavy_check_mark:                                                                   | The amount as a person reads it, with its currency.                                  |