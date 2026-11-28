# Question2

## Example Usage

```typescript
import { Question2 } from "bereach/models/operations";

let value: Question2 = {
  id: "<id>",
  question: "<value>",
  options: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `id`                                                                              | *string*                                                                          | :heavy_check_mark:                                                                | N/A                                                                               |
| `question`                                                                        | *string*                                                                          | :heavy_check_mark:                                                                | N/A                                                                               |
| `options`                                                                         | *string*[]                                                                        | :heavy_check_mark:                                                                | N/A                                                                               |
| `default`                                                                         | *string*                                                                          | :heavy_minus_sign:                                                                | What applies when the question is skipped; absent only when nothing can stand in. |