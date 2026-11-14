# GetDmPollingSettingsSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { GetDmPollingSettingsSpent } from "bereach/models/operations";

let value: GetDmPollingSettingsSpent = {
  amount: 1521.06,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `amount`                                                                                               | *number*                                                                                               | :heavy_check_mark:                                                                                     | The money spent.                                                                                       |
| `currency`                                                                                             | [operations.GetDmPollingSettingsCurrency](../../models/operations/get-dm-polling-settings-currency.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `text`                                                                                                 | *string*                                                                                               | :heavy_check_mark:                                                                                     | The amount as a person reads it, with its currency.                                                    |