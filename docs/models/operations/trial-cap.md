# TrialCap

The trial's cap, on a running trial; null otherwise

## Example Usage

```typescript
import { TrialCap } from "bereach/models/operations";

let value: TrialCap = {
  usedPercent: 1090.22,
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `usedPercent`                                                   | *number*                                                        | :heavy_check_mark:                                              | Share of the searches the trial includes already used, 0 to 100 |