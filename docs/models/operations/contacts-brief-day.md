# ContactsBriefDay

## Example Usage

```typescript
import { ContactsBriefDay } from "bereach/models/operations";

let value: ContactsBriefDay = {
  start: "<value>",
  end: "<value>",
  messages: 778065,
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