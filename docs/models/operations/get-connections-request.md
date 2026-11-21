# GetConnectionsRequest

## Example Usage

```typescript
import { GetConnectionsRequest } from "bereach/models/operations";

let value: GetConnectionsRequest = {};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `start`                                                        | *number*                                                       | :heavy_minus_sign:                                             | Pagination offset. Use the `nextStart` from the previous page. |
| `count`                                                        | *number*                                                       | :heavy_minus_sign:                                             | Results per page.                                              |
| `sortType`                                                     | [operations.SortType](../../models/operations/sort-type.md)    | :heavy_minus_sign:                                             | Sort order (default RECENTLY_ADDED)                            |