# SearchParametersRequest

## Example Usage

```typescript
import { SearchParametersRequest } from "bereach/models/operations";

let value: SearchParametersRequest = {
  type: "<value>",
};
```

## Fields

| Field                                                                                                                 | Type                                                                                                                  | Required                                                                                                              | Description                                                                                                           |
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `type`                                                                                                                | *string*                                                                                                              | :heavy_check_mark:                                                                                                    | Which kind of value to resolve. Entity kinds are looked up when asked; the closed-value kinds come from a fixed list. |
| `keywords`                                                                                                            | *string*                                                                                                              | :heavy_minus_sign:                                                                                                    | The text to resolve. Empty on a closed-value type lists every option.                                                 |
| `limit`                                                                                                               | *number*                                                                                                              | :heavy_minus_sign:                                                                                                    | N/A                                                                                                                   |