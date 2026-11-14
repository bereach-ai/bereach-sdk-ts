# Verbatim

## Example Usage

```typescript
import { Verbatim } from "bereach/models/operations";

let value: Verbatim = {
  direction: "received",
  at: "<value>",
  text: "<value>",
  senderName: "<value>",
};
```

## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `id`                                                         | *string*                                                     | :heavy_minus_sign:                                           | N/A                                                          |
| `direction`                                                  | [operations.Direction](../../models/operations/direction.md) | :heavy_check_mark:                                           | N/A                                                          |
| `at`                                                         | *string*                                                     | :heavy_check_mark:                                           | N/A                                                          |
| `text`                                                       | *string*                                                     | :heavy_check_mark:                                           | N/A                                                          |
| `senderName`                                                 | *string*                                                     | :heavy_check_mark:                                           | N/A                                                          |