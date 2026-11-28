# ContactsSearchPagination

## Example Usage

```typescript
import { ContactsSearchPagination } from "bereach/models/operations";

let value: ContactsSearchPagination = {
  limit: 600183,
  offset: 528931,
  total: 32618,
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `limit`                                                                                          | *number*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `offset`                                                                                         | *number*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `total`                                                                                          | *number*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `matched`                                                                                        | *number*                                                                                         | :heavy_minus_sign:                                                                               | Present only when total is capped to the rows that can be paged: how many people matched in all. |