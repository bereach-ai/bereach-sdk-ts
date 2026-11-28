# PatchDmPollingSettingsSpent

What this call spent, in money.

## Example Usage

```typescript
import { PatchDmPollingSettingsSpent } from "bereach/models/operations";

let value: PatchDmPollingSettingsSpent = {
  amount: 8756.51,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `amount`                                                                                                   | *number*                                                                                                   | :heavy_check_mark:                                                                                         | The money spent.                                                                                           |
| `currency`                                                                                                 | [operations.PatchDmPollingSettingsCurrency](../../models/operations/patch-dm-polling-settings-currency.md) | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `text`                                                                                                     | *string*                                                                                                   | :heavy_check_mark:                                                                                         | The amount as a person reads it, with its currency.                                                        |