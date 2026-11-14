# PublicFindPeopleSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { PublicFindPeopleSpent } from "bereach/models/operations";

let value: PublicFindPeopleSpent = {
  amount: 3733.11,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `amount`                                                                                      | *number*                                                                                      | :heavy_check_mark:                                                                            | The money spent.                                                                              |
| `currency`                                                                                    | [operations.PublicFindPeopleCurrency](../../models/operations/public-find-people-currency.md) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `text`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | The amount as a person reads it, with its currency.                                           |