# ActiveAccount

## Example Usage

```typescript
import { ActiveAccount } from "bereach/models/operations";

let value: ActiveAccount = {
  id: "<id>",
  name: "<value>",
  plan: "<value>",
  headline: "<value>",
  status: "connected",
  isUnlimited: true,
  simulateWrites: true,
  isCurrent: false,
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `id`                                                                               | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `name`                                                                             | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `plan`                                                                             | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `headline`                                                                         | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `status`                                                                           | [operations.ActiveAccountStatus](../../models/operations/active-account-status.md) | :heavy_check_mark:                                                                 | N/A                                                                                |
| `isUnlimited`                                                                      | *boolean*                                                                          | :heavy_check_mark:                                                                 | N/A                                                                                |
| `simulateWrites`                                                                   | *boolean*                                                                          | :heavy_check_mark:                                                                 | N/A                                                                                |
| `isCurrent`                                                                        | *boolean*                                                                          | :heavy_check_mark:                                                                 | N/A                                                                                |