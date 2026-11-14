# RunSearchesPerson

## Example Usage

```typescript
import { RunSearchesPerson } from "bereach/models/operations";

let value: RunSearchesPerson = {
  name: "<value>",
  profile: "<value>",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `name`                                                                             | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `title`                                                                            | *string*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |
| `headline`                                                                         | *string*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |
| `company`                                                                          | *string*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |
| `place`                                                                            | *string*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |
| `profile`                                                                          | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `slug`                                                                             | *string*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |
| `contactId`                                                                        | *string*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |
| `avatar`                                                                           | *string*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |
| `employer`                                                                         | [operations.RunSearchesEmployer](../../models/operations/run-searches-employer.md) | :heavy_minus_sign:                                                                 | The person's current employer, from that company's own record.                     |
| `employerUnread`                                                                   | [operations.EmployerUnread](../../models/operations/employer-unread.md)            | :heavy_minus_sign:                                                                 | Why this person carries no employer facts.                                         |
| `inListBefore`                                                                     | *true*                                                                             | :heavy_minus_sign:                                                                 | Already in this list before this run.                                              |