# RecentEvent

## Example Usage

```typescript
import { RecentEvent } from "bereach/models/operations";

let value: RecentEvent = {
  id: "<id>",
  type: "credential:linkedin_long_broken",
  summary: "<value>",
  metadata: {},
  timestamp: 8667.67,
};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `id`                                                                     | *string*                                                                 | :heavy_check_mark:                                                       | N/A                                                                      |
| `type`                                                                   | [operations.ContextGetType](../../models/operations/context-get-type.md) | :heavy_check_mark:                                                       | N/A                                                                      |
| `campaignId`                                                             | *string*                                                                 | :heavy_minus_sign:                                                       | N/A                                                                      |
| `campaignName`                                                           | *string*                                                                 | :heavy_minus_sign:                                                       | N/A                                                                      |
| `summary`                                                                | *string*                                                                 | :heavy_check_mark:                                                       | Human-readable one-line summary                                          |
| `metadata`                                                               | Record<string, *any*>                                                    | :heavy_check_mark:                                                       | N/A                                                                      |
| `timestamp`                                                              | *number*                                                                 | :heavy_check_mark:                                                       | Unix epoch ms                                                            |