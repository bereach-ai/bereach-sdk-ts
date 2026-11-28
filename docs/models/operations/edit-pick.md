# EditPick

## Example Usage

```typescript
import { EditPick } from "bereach/models/operations";

let value: EditPick = {
  op: "pick",
  icp: "<value>",
  field: "kinds",
  value: "<value>",
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `op`                                                   | *"pick"*                                               | :heavy_check_mark:                                     | N/A                                                    |
| `icp`                                                  | *string*                                               | :heavy_check_mark:                                     | N/A                                                    |
| `field`                                                | [operations.Field2](../../models/operations/field2.md) | :heavy_check_mark:                                     | N/A                                                    |
| `value`                                                | *string*                                               | :heavy_check_mark:                                     | N/A                                                    |