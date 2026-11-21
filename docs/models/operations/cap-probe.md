# CapProbe

Set only while LinkedIn's own invitation ceiling is what stopped this account

## Example Usage

```typescript
import { CapProbe } from "bereach/models/operations";

let value: CapProbe = {
  nextProbeAt: "<value>",
  rung: 411852,
  finalRung: 388876,
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `nextProbeAt`                                                                       | *string*                                                                            | :heavy_check_mark:                                                                  | When LinkedIn is asked again                                                        |
| `rung`                                                                              | *number*                                                                            | :heavy_check_mark:                                                                  | How far the wait between checks has widened                                         |
| `finalRung`                                                                         | *number*                                                                            | :heavy_check_mark:                                                                  | The widest it gets. Checks continue at that spacing until sending is allowed again. |