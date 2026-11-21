# Summary

## Example Usage

```typescript
import { Summary } from "bereach/models/operations";

let value: Summary = {
  days: [
    {
      start: "<value>",
      end: "<value>",
      messages: 399543,
      summary: "<value>",
    },
  ],
  weeks: [
    {
      start: "<value>",
      end: "<value>",
      messages: 962975,
      summary: "<value>",
    },
  ],
  months: [
    {
      start: "<value>",
      end: "<value>",
      messages: 837152,
      summary: "<value>",
    },
  ],
  waiting: 803884,
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `days`                                                                           | [operations.ContactsBriefDay](../../models/operations/contacts-brief-day.md)[]   | :heavy_check_mark:                                                               | N/A                                                                              |
| `weeks`                                                                          | [operations.ContactsBriefWeek](../../models/operations/contacts-brief-week.md)[] | :heavy_check_mark:                                                               | N/A                                                                              |
| `months`                                                                         | [operations.Month](../../models/operations/month.md)[]                           | :heavy_check_mark:                                                               | N/A                                                                              |
| `waiting`                                                                        | *number*                                                                         | :heavy_check_mark:                                                               | Periods whose summary waits for a later brief.                                   |