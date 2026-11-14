# SearchCompaniesPaging

## Example Usage

```typescript
import { SearchCompaniesPaging } from "bereach/models/operations";

let value: SearchCompaniesPaging = {
  start: 823293,
  count: 432640,
  total: 848721,
};
```

## Fields

| Field                                                      | Type                                                       | Required                                                   | Description                                                |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| `start`                                                    | *number*                                                   | :heavy_check_mark:                                         | The offset asked.                                          |
| `count`                                                    | *number*                                                   | :heavy_check_mark:                                         | How many items this page returned.                         |
| `total`                                                    | *number*                                                   | :heavy_check_mark:                                         | Always null: the provider does not count the whole market. |