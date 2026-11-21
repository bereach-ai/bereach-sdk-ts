# LatestRound

The company's latest funding round. Only on a search that carried a funding window.

## Example Usage

```typescript
import { LatestRound } from "bereach/models/operations";

let value: LatestRound = {
  name: "<value>",
  date: "2024-05-13",
  amount: 9320.71,
};
```

## Fields

| Field                                           | Type                                            | Required                                        | Description                                     |
| ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- |
| `name`                                          | *string*                                        | :heavy_check_mark:                              | The kind of round, as recorded.                 |
| `date`                                          | *string*                                        | :heavy_check_mark:                              | The date of the round, exactly as recorded.     |
| `amount`                                        | *number*                                        | :heavy_check_mark:                              | The amount raised in US dollars, when recorded. |