# MessageHours

The user's working hours, which messages follow. Null returns to the usual hours. Left out, they stay as they are.

## Example Usage

```typescript
import { MessageHours } from "bereach/models/operations";

let value: MessageHours = {
  from: 635560,
  to: 358837,
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `from`                                                                                | *number*                                                                              | :heavy_check_mark:                                                                    | The whole hour, local, when messages may start.                                       |
| `to`                                                                                  | *number*                                                                              | :heavy_check_mark:                                                                    | The whole hour, local, when they stop; 24 is midnight. From 5 to 16 hours after from. |