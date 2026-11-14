# EditRemove

## Example Usage

```typescript
import { EditRemove } from "bereach/models/operations";

let value: EditRemove = {
  op: "remove",
  field: "peopleWanted",
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `op`                                                   | *"remove"*                                             | :heavy_check_mark:                                     | N/A                                                    |
| `field`                                                | [operations.Field1](../../models/operations/field1.md) | :heavy_check_mark:                                     | N/A                                                    |
| `icp`                                                  | *string*                                               | :heavy_minus_sign:                                     | N/A                                                    |
| `id`                                                   | *string*                                               | :heavy_minus_sign:                                     | N/A                                                    |
| `value`                                                | *string*                                               | :heavy_minus_sign:                                     | N/A                                                    |