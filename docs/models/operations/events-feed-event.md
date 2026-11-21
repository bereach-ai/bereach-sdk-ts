# EventsFeedEvent

## Example Usage

```typescript
import { EventsFeedEvent } from "bereach/models/operations";

let value: EventsFeedEvent = {
  id: "<id>",
  type: "credential:llm_error",
  summary: "<value>",
  metadata: {
    "key": "<value>",
    "key1": "<value>",
  },
  timestamp: 3693.54,
};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `id`                                                                     | *string*                                                                 | :heavy_check_mark:                                                       | N/A                                                                      |
| `type`                                                                   | [operations.EventsFeedType](../../models/operations/events-feed-type.md) | :heavy_check_mark:                                                       | N/A                                                                      |
| `campaignId`                                                             | *string*                                                                 | :heavy_minus_sign:                                                       | N/A                                                                      |
| `campaignName`                                                           | *string*                                                                 | :heavy_minus_sign:                                                       | N/A                                                                      |
| `summary`                                                                | *string*                                                                 | :heavy_check_mark:                                                       | Human-readable one-line summary                                          |
| `metadata`                                                               | Record<string, *any*>                                                    | :heavy_check_mark:                                                       | N/A                                                                      |
| `timestamp`                                                              | *number*                                                                 | :heavy_check_mark:                                                       | Unix epoch ms                                                            |