# Window

The five-hour usage limit on paid reads, on a trial, a plan or the free tier

## Example Usage

```typescript
import { Window } from "bereach/models/operations";

let value: Window = {
  usedPercent: 7863.62,
  resetsAt: "<value>",
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `usedPercent`                                                                                              | *number*                                                                                                   | :heavy_check_mark:                                                                                         | Share of the five-hour usage limit used, 0 to 100                                                          |
| `resetsAt`                                                                                                 | *string*                                                                                                   | :heavy_check_mark:                                                                                         | When the five-hour usage limit resets, ISO; null when no window is open (it opens with the next paid read) |