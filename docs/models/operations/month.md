# Month

## Example Usage

```typescript
import { Month } from "bereach/models/operations";

let value: Month = {
  start: "<value>",
  end: "<value>",
  messages: 996326,
  summary: "<value>",
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `start`                                                  | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `end`                                                    | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `messages`                                               | *number*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `summary`                                                | *string*                                                 | :heavy_check_mark:                                       | Null when this period's summary waits for a later brief. |