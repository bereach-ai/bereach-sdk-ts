# SetTimeZoneSpent

What this call spent, in money.

## Example Usage

```typescript
import { SetTimeZoneSpent } from "bereach/models/operations";

let value: SetTimeZoneSpent = {
  amount: 2582.35,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `amount`                                                                            | *number*                                                                            | :heavy_check_mark:                                                                  | The money spent.                                                                    |
| `currency`                                                                          | [operations.SetTimeZoneCurrency](../../models/operations/set-time-zone-currency.md) | :heavy_check_mark:                                                                  | N/A                                                                                 |
| `text`                                                                              | *string*                                                                            | :heavy_check_mark:                                                                  | The amount as a person reads it, with its currency.                                 |