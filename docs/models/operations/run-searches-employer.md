# RunSearchesEmployer

The person's current employer, from that company's own record.

## Example Usage

```typescript
import { RunSearchesEmployer } from "bereach/models/operations";

let value: RunSearchesEmployer = {};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `name`                                                                 | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `employees`                                                            | *number*                                                               | :heavy_minus_sign:                                                     | How many people the company employs, by its own record.                |
| `industry`                                                             | *string*                                                               | :heavy_minus_sign:                                                     | What kind of company it is, by its own record.                         |
| `hq`                                                                   | [operations.RunSearchesHq](../../models/operations/run-searches-hq.md) | :heavy_minus_sign:                                                     | Where its headquarters are.                                            |
| `founded`                                                              | *number*                                                               | :heavy_minus_sign:                                                     | The year it was founded.                                               |
| `page`                                                                 | *string*                                                               | :heavy_minus_sign:                                                     | The company's own page.                                                |
| `website`                                                              | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |