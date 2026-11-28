# Question1

## Example Usage

```typescript
import { Question1 } from "bereach/models/operations";

let value: Question1 = {
  id: "<id>",
  question: "<value>",
  options: [],
};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `id`                                                                              | *string*                                                                          | :heavy_check_mark:                                                                | N/A                                                                               |
| `question`                                                                        | *string*                                                                          | :heavy_check_mark:                                                                | N/A                                                                               |
| `options`                                                                         | *string*[]                                                                        | :heavy_check_mark:                                                                | N/A                                                                               |
| `default`                                                                         | *string*                                                                          | :heavy_minus_sign:                                                                | What applies when the question is skipped; absent only when nothing can stand in. |