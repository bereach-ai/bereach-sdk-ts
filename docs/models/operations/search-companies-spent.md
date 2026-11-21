# SearchCompaniesSpent

What this call spent, in money.

## Example Usage

```typescript
import { SearchCompaniesSpent } from "bereach/models/operations";

let value: SearchCompaniesSpent = {
  amount: 2229.29,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `amount`                                                                                   | *number*                                                                                   | :heavy_check_mark:                                                                         | The money spent.                                                                           |
| `currency`                                                                                 | [operations.SearchCompaniesCurrency](../../models/operations/search-companies-currency.md) | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `text`                                                                                     | *string*                                                                                   | :heavy_check_mark:                                                                         | The amount as a person reads it, with its currency.                                        |