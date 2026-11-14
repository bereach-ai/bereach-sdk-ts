# Progress

The run this call started, else the last run, or null when the list never had one.

## Example Usage

```typescript
import { Progress } from "bereach/models/operations";

let value: Progress = {
  state: "stopped",
  total: 340252,
  peopleRead: 238665,
  companies: 685450,
  companiesRead: 740187,
  found: 186527,
  credits: 1398.36,
  startedAt: "<value>",
};
```

## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `state`                                                               | [operations.ProgressState](../../models/operations/progress-state.md) | :heavy_check_mark:                                                    | N/A                                                                   |
| `total`                                                               | *number*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `peopleRead`                                                          | *number*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `companies`                                                           | *number*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `companiesRead`                                                       | *number*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `found`                                                               | *number*                                                              | :heavy_check_mark:                                                    | People who got a reason.                                              |
| `credits`                                                             | *number*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `startedAt`                                                           | *string*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `endedAt`                                                             | *string*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |