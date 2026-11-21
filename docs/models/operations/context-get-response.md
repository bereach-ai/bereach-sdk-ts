# ContextGetResponse

Session snapshot

## Example Usage

```typescript
import { ContextGetResponse } from "bereach/models/operations";

let value: ContextGetResponse = {
  pipeline: {
    "key": 168068,
  },
  contexts: [
    {
      type: "<value>",
      label: "<value>",
      content: "<value>",
      scope: "<value>",
    },
  ],
  pendingDrafts: 890607,
  failedDrafts: 331104,
  pendingSentInvitations: 547720,
  activeAccount: {
    id: "<id>",
    name: "<value>",
    plan: "<value>",
    headline: null,
    status: "expired",
    isUnlimited: false,
    simulateWrites: true,
    isCurrent: true,
  },
  accounts: [
    {
      id: "<id>",
      name: "<value>",
      plan: "<value>",
      headline: null,
      status: "connected",
      isUnlimited: true,
      simulateWrites: true,
      isCurrent: false,
    },
  ],
  activeCampaigns: [],
  recentEvents: [],
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `pipeline`                                                                                                 | Record<string, *number*>                                                                                   | :heavy_check_mark:                                                                                         | List memberships counted by stage, with a total that includes removed. A person on two lists counts twice. |
| `contexts`                                                                                                 | [operations.Context](../../models/operations/context.md)[]                                                 | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `pendingDrafts`                                                                                            | *number*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `failedDrafts`                                                                                             | *number*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `pendingSentInvitations`                                                                                   | *number*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `activeAccount`                                                                                            | [operations.ActiveAccount](../../models/operations/active-account.md)                                      | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `accounts`                                                                                                 | [operations.ContextGetAccount](../../models/operations/context-get-account.md)[]                           | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `activeCampaigns`                                                                                          | [operations.ActiveCampaign](../../models/operations/active-campaign.md)[]                                  | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `recentEvents`                                                                                             | [operations.RecentEvent](../../models/operations/recent-event.md)[]                                        | :heavy_check_mark:                                                                                         | N/A                                                                                                        |