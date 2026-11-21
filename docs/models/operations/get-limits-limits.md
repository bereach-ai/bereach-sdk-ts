# GetLimitsLimits

## Example Usage

```typescript
import { GetLimitsLimits } from "bereach/models/operations";

let value: GetLimitsLimits = {
  connectionRequest: {
    uncapped: true,
    daily: null,
    weekly: {
      current: 905903,
      limit: 617573,
      remaining: 804803,
    },
    minIntervalSeconds: 426412,
    nextResetDaily: "<value>",
    nextResetWeekly: "<value>",
  },
  message: {
    uncapped: false,
    daily: {
      current: 567882,
      limit: 669069,
      remaining: 636753,
    },
    weekly: {
      current: 534020,
      limit: 472297,
      remaining: 863521,
    },
    minIntervalSeconds: 48135,
    nextResetDaily: "<value>",
    nextResetWeekly: "<value>",
  },
  profileVisit: {
    uncapped: false,
    daily: {
      current: 293170,
      limit: 692882,
      remaining: 96344,
    },
    weekly: {
      current: 791982,
      limit: 483792,
      remaining: 394394,
    },
    minIntervalSeconds: 440440,
    nextResetDaily: null,
    nextResetWeekly: "<value>",
  },
  scraping: {
    uncapped: false,
    daily: {
      current: 137081,
      limit: 85944,
      remaining: 814423,
    },
    weekly: null,
    minIntervalSeconds: 811262,
    nextResetDaily: null,
    nextResetWeekly: "<value>",
  },
};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `connectionRequest`                                                             | [operations.ConnectionRequest](../../models/operations/connection-request.md)   | :heavy_check_mark:                                                              | Limits for sending LinkedIn connection requests                                 |
| `message`                                                                       | [operations.GetLimitsMessage](../../models/operations/get-limits-message.md)    | :heavy_check_mark:                                                              | Limits for sending DMs                                                          |
| `profileVisit`                                                                  | [operations.ProfileVisit](../../models/operations/profile-visit.md)             | :heavy_check_mark:                                                              | Limits for the optional degree details and the check before an invitation.      |
| `scraping`                                                                      | [operations.Scraping](../../models/operations/scraping.md)                      | :heavy_check_mark:                                                              | Limits for searches and for reading your own network and posts.                 |
| `acceptInvitation`                                                              | [operations.AcceptInvitation](../../models/operations/accept-invitation.md)     | :heavy_minus_sign:                                                              | Limits for accepting connection invitations                                     |
| `withdrawInvitation`                                                            | [operations.WithdrawInvitation](../../models/operations/withdraw-invitation.md) | :heavy_minus_sign:                                                              | Limits for withdrawing sent connection invitations                              |
| `profile`                                                                       | [operations.GetLimitsProfile](../../models/operations/get-limits-profile.md)    | :heavy_minus_sign:                                                              | Limits for profile actions.                                                     |