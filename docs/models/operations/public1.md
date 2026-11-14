# Public1

## Example Usage

```typescript
import { Public1 } from "bereach/models/operations";

let value: Public1 = {
  source: "public",
  creditsUsed: 726644,
  completeness: "<value>",
  saved: false,
  profile: {
    "key": "<value>",
  },
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `source`                                                                                                                             | [operations.PublicProfileSource1](../../models/operations/public-profile-source1.md)                                                 | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.PublicProfileSpent1](../../models/operations/public-profile-spent1.md)                                                   | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `readFrom`                                                                                                                           | [operations.PublicProfileReadFrom](../../models/operations/public-profile-read-from.md)                                              | :heavy_minus_sign:                                                                                                                   | Where a profile read in full was read: the record a search of yours already saved, or a public record read today.                    |
| `readAt`                                                                                                                             | *string*                                                                                                                             | :heavy_minus_sign:                                                                                                                   | For a profile from a saved search record: when it was read, so how old the profile is.                                               |
| `completeness`                                                                                                                       | *string*                                                                                                                             | :heavy_check_mark:                                                                                                                   | How complete the fetched public profile is.                                                                                          |
| `saved`                                                                                                                              | *boolean*                                                                                                                            | :heavy_check_mark:                                                                                                                   | Whether the profile was saved to your contacts.                                                                                      |
| `profile`                                                                                                                            | Record<string, *any*>                                                                                                                | :heavy_check_mark:                                                                                                                   | The profile data.                                                                                                                    |