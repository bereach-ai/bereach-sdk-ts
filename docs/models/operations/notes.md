# Notes

This account's personal notes on invitations. A note LinkedIn will not take is left off and the invitation is still sent, so this is never a block.

## Example Usage

```typescript
import { Notes } from "bereach/models/operations";

let value: Notes = {
  usedUp: false,
  nextTryAt: "<value>",
  maxLength: 110906,
  sentWithoutNote30d: 184784,
  message: "<value>",
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `usedUp`                                                                                              | *boolean*                                                                                             | :heavy_check_mark:                                                                                    | LinkedIn's monthly allowance of personal notes is used up, so invitations are sent without their note |
| `nextTryAt`                                                                                           | *string*                                                                                              | :heavy_check_mark:                                                                                    | When an invitation is next tried with its note, while notes are used up                               |
| `maxLength`                                                                                           | *number*                                                                                              | :heavy_check_mark:                                                                                    | The longest note this account accepts, known once LinkedIn has refused a longer one                   |
| `sentWithoutNote30d`                                                                                  | *number*                                                                                              | :heavy_check_mark:                                                                                    | Invitations sent without the note that was written for them, in the last 30 days                      |
| `message`                                                                                             | *string*                                                                                              | :heavy_check_mark:                                                                                    | One sentence saying all of this, suitable to show as written                                          |