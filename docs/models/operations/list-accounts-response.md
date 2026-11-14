# ListAccountsResponse

List of LinkedIn accounts

## Example Usage

```typescript
import { ListAccountsResponse } from "bereach/models/operations";

let value: ListAccountsResponse = {
  success: true,
  accounts: [
    {
      id: "<id>",
      label: null,
      isDefault: true,
      isCurrent: false,
      linkedinProfileId: "<id>",
      linkedinName: "<value>",
      linkedinEmail: "<value>",
      profileUrl: "https://snappy-numeric.com/",
      headline: "<value>",
      profilePic: "<value>",
      profileUrn: "<value>",
      isActive: true,
      isValid: false,
      accountPlan: "<value>",
      isUnlimited: true,
      proxyConfig: {
        enabled: false,
      },
      createdAt: "1711331755229",
      updatedAt: "1735680327784",
    },
  ],
  total: 436562,
  isOwner: true,
  creditsUsed: 591899,
  retryAfter: 653111,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `accounts`                                                                                                                           | [operations.ListAccountsAccount](../../models/operations/list-accounts-account.md)[]                                                 | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `total`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `isOwner`                                                                                                                            | *boolean*                                                                                                                            | :heavy_check_mark:                                                                                                                   | True when the caller owns the workspace, in which case `accounts` spans the whole workspace rather than just their own.              |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ListAccountsSpent](../../models/operations/list-accounts-spent.md)                                                       | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |