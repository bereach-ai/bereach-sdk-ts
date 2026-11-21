# AcceptInvitationSpent

What this call spent, in money.

## Example Usage

```typescript
import { AcceptInvitationSpent } from "bereach/models/operations";

let value: AcceptInvitationSpent = {
  amount: 7909.79,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `amount`                                                                                     | *number*                                                                                     | :heavy_check_mark:                                                                           | The money spent.                                                                             |
| `currency`                                                                                   | [operations.AcceptInvitationCurrency](../../models/operations/accept-invitation-currency.md) | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `text`                                                                                       | *string*                                                                                     | :heavy_check_mark:                                                                           | The amount as a person reads it, with its currency.                                          |