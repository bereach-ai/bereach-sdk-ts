# SearchPostsPaging

## Example Usage

```typescript
import { SearchPostsPaging } from "bereach/models/operations";

let value: SearchPostsPaging = {
  start: 200389,
  count: 747889,
  total: 419423,
};
```

## Fields

| Field                                                      | Type                                                       | Required                                                   | Description                                                |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| `start`                                                    | *number*                                                   | :heavy_check_mark:                                         | The offset asked.                                          |
| `count`                                                    | *number*                                                   | :heavy_check_mark:                                         | How many items this page returned.                         |
| `total`                                                    | *number*                                                   | :heavy_check_mark:                                         | Always null: the provider does not count the whole market. |