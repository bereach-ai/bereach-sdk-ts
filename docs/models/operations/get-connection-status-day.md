# GetConnectionStatusDay

## Example Usage

```typescript
import { GetConnectionStatusDay } from "bereach/models/operations";

let value: GetConnectionStatusDay = {
  start: "<value>",
  counting: true,
  invitations: {
    sent: 920267,
    won: 643040,
    rate: 201810,
    withNote: {
      sent: 673473,
      won: 717846,
      rate: 876690,
    },
    withoutNote: {
      sent: 730592,
      won: 758126,
      rate: 83839,
    },
  },
  firstMessages: {
    sent: 103756,
    won: 912584,
    rate: 309656,
  },
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `start`                                                                        | *string*                                                                       | :heavy_check_mark:                                                             | First day of the period, UTC; a week starts on Monday                          |
| `counting`                                                                     | *boolean*                                                                      | :heavy_check_mark:                                                             | Still inside withinDays past its end, so not yet comparable with older periods |
| `invitations`                                                                  | [operations.DayInvitations](../../models/operations/day-invitations.md)        | :heavy_check_mark:                                                             | N/A                                                                            |
| `firstMessages`                                                                | [operations.DayFirstMessages](../../models/operations/day-first-messages.md)   | :heavy_check_mark:                                                             | N/A                                                                            |