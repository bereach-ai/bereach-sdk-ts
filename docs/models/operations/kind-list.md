# KindList

## Example Usage

```typescript
import { KindList } from "bereach/models/operations";

let value: KindList = {
  said: "<id>",
  industries: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `said`                                                      | *string*                                                    | :heavy_check_mark:                                          | Their own words for this kind, as written.                  |
| `industries`                                                | *string*[]                                                  | :heavy_check_mark:                                          | The LinkedIn industry names such companies are filed under. |