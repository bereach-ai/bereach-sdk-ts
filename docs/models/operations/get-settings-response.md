# GetSettingsResponse

Account settings

## Example Usage

```typescript
import { GetSettingsResponse } from "bereach/models/operations";

let value: GetSettingsResponse = {
  success: true,
  isAdmin: true,
  user: {
    id: "<id>",
    name: "<value>",
    email: "Uriel.Berge@yahoo.com",
    image: "https://picsum.photos/seed/Kf8Mcy/2366/3723",
    phone: "346.329.6101 x73797",
    createdAt: "1724917292460",
  },
  location: {
    country: "Uzbekistan",
    city: null,
  },
  proxy: {
    enabled: false,
  },
  subscription: {
    plan: "<value>",
    tier: "<value>",
    proSeatsIncluded: 182301,
    proSeatsUsed: 430854,
    status: "<value>",
    currentPeriodEnd: "<value>",
    hasStripe: false,
  },
  linkedinAccounts: [
    {
      id: "<id>",
      label: null,
      isDefault: false,
      linkedinName: "<value>",
      linkedinEmail: "<value>",
      profilePic: "<value>",
      profileUrl: "https://dazzling-cellar.net/",
      headline: "<value>",
      isValid: true,
      isActive: false,
      validationError: "<value>",
      accountPlan: "<value>",
      isUnlimited: true,
      proxy: {
        enabled: true,
      },
      apiKey: {
        partialKey: "<value>",
        createdAt: "1725560521212",
      },
      createdAt: "1727121484903",
    },
  ],
  pendingInvites: [
    {
      id: "<id>",
      email: "Darrion.Reichel37@yahoo.com",
      name: "<value>",
      code: "<value>",
      maxUses: 341653,
      useCount: 301631,
      expiresAt: "1743286578554",
      createdAt: "1730024896275",
    },
  ],
  workspaceMembers: [
    {
      id: "<id>",
      name: "<value>",
      email: "Brandt11@yahoo.com",
      isOwner: false,
      role: "member",
    },
  ],
};
```

## Fields

| Field                                                                                                                               | Type                                                                                                                                | Required                                                                                                                            | Description                                                                                                                         |
| ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                           | *true*                                                                                                                              | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `isAdmin`                                                                                                                           | *boolean*                                                                                                                           | :heavy_check_mark:                                                                                                                  | Whether this workspace has BeReach-staff admin-panel access. The SAME value for every member of a workspace: not a per-member role. |
| `user`                                                                                                                              | [operations.User](../../models/operations/user.md)                                                                                  | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `location`                                                                                                                          | [operations.GetSettingsLocation](../../models/operations/get-settings-location.md)                                                  | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `proxy`                                                                                                                             | [operations.Proxy](../../models/operations/proxy.md)                                                                                | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `subscription`                                                                                                                      | [operations.Subscription](../../models/operations/subscription.md)                                                                  | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `linkedinAccounts`                                                                                                                  | [operations.LinkedinAccount](../../models/operations/linkedin-account.md)[]                                                         | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `pendingInvites`                                                                                                                    | [operations.PendingInvite](../../models/operations/pending-invite.md)[]                                                             | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `workspaceMembers`                                                                                                                  | [operations.WorkspaceMember](../../models/operations/workspace-member.md)[]                                                         | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |