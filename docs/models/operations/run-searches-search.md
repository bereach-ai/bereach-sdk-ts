# RunSearchesSearch

## Example Usage

```typescript
import { RunSearchesSearch } from "bereach/models/operations";

let value: RunSearchesSearch = {
  id: "<id>",
  icp: "<value>",
  rank: 997780,
  label: "<value>",
  state: "searching",
  added: 852281,
  queriesRun: 336065,
  queriesPlanned: 362598,
};
```

## Fields

| Field                                                             | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `id`                                                              | *string*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `icp`                                                             | *string*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `rank`                                                            | *number*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `label`                                                           | *string*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `state`                                                           | [operations.SearchState](../../models/operations/search-state.md) | :heavy_check_mark:                                                | N/A                                                               |
| `added`                                                           | *number*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `queriesRun`                                                      | *number*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `queriesPlanned`                                                  | *number*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `note`                                                            | *string*                                                          | :heavy_minus_sign:                                                | N/A                                                               |