# TopUp

The money added by card, a bucket of its own

## Example Usage

```typescript
import { TopUp } from "bereach/models/operations";

let value: TopUp = {
  left: true,
  limited: false,
};
```

## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `left`                                                                | *boolean*                                                             | :heavy_check_mark:                                                    | Whether enough money added by card is left to pay for a paid read now |
| `limited`                                                             | *false*                                                               | :heavy_check_mark:                                                    | Never held by a limit: only what is left of it bounds it              |