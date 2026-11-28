# NotSearched

## Example Usage

```typescript
import { NotSearched } from "bereach/models/operations";

let value: NotSearched = {
  field: "<value>",
  value: "<value>",
  why: "<value>",
  effect: "<value>",
};
```

## Fields

| Field                                                             | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `field`                                                           | *string*                                                          | :heavy_check_mark:                                                | The constraint that could not be applied.                         |
| `value`                                                           | *string*                                                          | :heavy_check_mark:                                                | What was asked for.                                               |
| `why`                                                             | *string*                                                          | :heavy_check_mark:                                                | Why it could not be applied, in plain words.                      |
| `effect`                                                          | *string*                                                          | :heavy_check_mark:                                                | What that does to the results: wider than asked, never different. |