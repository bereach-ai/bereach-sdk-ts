# GetConnectionStatusWeek

## Example Usage

```typescript
import { GetConnectionStatusWeek } from "bereach/models/operations";

let value: GetConnectionStatusWeek = {
  start: "<value>",
  counting: false,
  invitations: {
    sent: 211286,
    won: 951293,
    rate: 789951,
    withNote: {
      sent: 980177,
      won: 879935,
      rate: 434505,
    },
    withoutNote: {
      sent: 802418,
      won: 805254,
      rate: 225083,
    },
  },
  firstMessages: {
    sent: 441115,
    won: 26989,
    rate: 665795,
  },
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `start`                                                                        | *string*                                                                       | :heavy_check_mark:                                                             | First day of the period, UTC; a week starts on Monday                          |
| `counting`                                                                     | *boolean*                                                                      | :heavy_check_mark:                                                             | Still inside withinDays past its end, so not yet comparable with older periods |
| `invitations`                                                                  | [operations.WeekInvitations](../../models/operations/week-invitations.md)      | :heavy_check_mark:                                                             | N/A                                                                            |
| `firstMessages`                                                                | [operations.WeekFirstMessages](../../models/operations/week-first-messages.md) | :heavy_check_mark:                                                             | N/A                                                                            |