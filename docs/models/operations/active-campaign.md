# ActiveCampaign

## Example Usage

```typescript
import { ActiveCampaign } from "bereach/models/operations";

let value: ActiveCampaign = {
  id: "<id>",
  name: "<value>",
  stageCounts: {
    contact: 434825,
    lead: 724861,
    qualified: 956973,
    rejected: 918675,
    total: 652290,
  },
};
```

## Fields

| Field                                                                                   | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `id`                                                                                    | *string*                                                                                | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `name`                                                                                  | *string*                                                                                | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `stageCounts`                                                                           | [operations.ContextGetStageCounts](../../models/operations/context-get-stage-counts.md) | :heavy_check_mark:                                                                      | N/A                                                                                     |