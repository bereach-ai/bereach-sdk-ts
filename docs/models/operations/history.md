# History

## Example Usage

```typescript
import { History } from "bereach/models/operations";

let value: History = {
  found: true,
  readFrom: "stored",
  verbatim: [
    {
      direction: "received",
      at: "<value>",
      text: "<value>",
      senderName: "<value>",
    },
  ],
  summary: {
    days: [],
    weeks: [
      {
        start: "<value>",
        end: "<value>",
        messages: 962975,
        summary: "<value>",
      },
    ],
    months: [],
    waiting: 739286,
  },
  totalMessages: 79436,
  oldestAt: null,
  complete: false,
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `found`                                                                    | *boolean*                                                                  | :heavy_check_mark:                                                         | N/A                                                                        |
| `reason`                                                                   | [operations.HistoryReason](../../models/operations/history-reason.md)      | :heavy_minus_sign:                                                         | Why this part is empty or older than asked.                                |
| `readFrom`                                                                 | [operations.HistoryReadFrom](../../models/operations/history-read-from.md) | :heavy_check_mark:                                                         | N/A                                                                        |
| `verbatim`                                                                 | [operations.Verbatim](../../models/operations/verbatim.md)[]               | :heavy_check_mark:                                                         | The latest messages, oldest first, whole.                                  |
| `summary`                                                                  | [operations.Summary](../../models/operations/summary.md)                   | :heavy_check_mark:                                                         | N/A                                                                        |
| `totalMessages`                                                            | *number*                                                                   | :heavy_check_mark:                                                         | N/A                                                                        |
| `oldestAt`                                                                 | *string*                                                                   | :heavy_check_mark:                                                         | N/A                                                                        |
| `complete`                                                                 | *boolean*                                                                  | :heavy_check_mark:                                                         | The whole conversation, back to its first message, is held.                |