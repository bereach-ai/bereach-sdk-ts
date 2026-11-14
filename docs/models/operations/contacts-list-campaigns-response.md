# ContactsListCampaignsResponse

Campaigns list

## Example Usage

```typescript
import { ContactsListCampaignsResponse } from "bereach/models/operations";

let value: ContactsListCampaignsResponse = {
  success: true,
  campaigns: [],
  pagination: {
    limit: 46073,
    offset: 486417,
    total: 181531,
  },
  creditsUsed: 368013,
  retryAfter: 442399,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `campaigns`                                                                                                                          | [operations.ContactsListCampaignsCampaign](../../models/operations/contacts-list-campaigns-campaign.md)[]                            | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `pagination`                                                                                                                         | [operations.ContactsListCampaignsPagination](../../models/operations/contacts-list-campaigns-pagination.md)                          | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ContactsListCampaignsSpent](../../models/operations/contacts-list-campaigns-spent.md)                                    | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |