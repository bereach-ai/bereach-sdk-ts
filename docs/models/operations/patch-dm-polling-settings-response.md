# PatchDmPollingSettingsResponse

Settings updated

## Example Usage

```typescript
import { PatchDmPollingSettingsResponse } from "bereach/models/operations";

let value: PatchDmPollingSettingsResponse = {
  success: true,
  settings: {
    dmWebhookUrl: "https://rotating-necklace.biz",
    connectionLastPolledAt: "<value>",
  },
  creditsUsed: 335675,
  retryAfter: 768553,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `settings`                                                                                                                           | [operations.PatchDmPollingSettingsSettings](../../models/operations/patch-dm-polling-settings-settings.md)                           | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.PatchDmPollingSettingsSpent](../../models/operations/patch-dm-polling-settings-spent.md)                                 | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |