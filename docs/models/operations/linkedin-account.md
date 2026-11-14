# LinkedinAccount

## Example Usage

```typescript
import { LinkedinAccount } from "bereach/models/operations";

let value: LinkedinAccount = {
  id: "<id>",
  label: "<value>",
  isDefault: true,
  linkedinName: "<value>",
  linkedinEmail: "<value>",
  profilePic: "<value>",
  profileUrl: "https://cool-outrun.name",
  headline: "<value>",
  isValid: false,
  isActive: true,
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
  createdAt: "1725024920437",
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `id`                                                                                         | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `label`                                                                                      | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `isDefault`                                                                                  | *boolean*                                                                                    | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `linkedinName`                                                                               | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `linkedinEmail`                                                                              | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `profilePic`                                                                                 | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `profileUrl`                                                                                 | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `headline`                                                                                   | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `isValid`                                                                                    | *boolean*                                                                                    | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `isActive`                                                                                   | *boolean*                                                                                    | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `validationError`                                                                            | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `accountPlan`                                                                                | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `isUnlimited`                                                                                | *boolean*                                                                                    | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `ownedByCaller`                                                                              | *boolean*                                                                                    | :heavy_minus_sign:                                                                           | True when this account belongs to the caller rather than to another member of the workspace. |
| `proxy`                                                                                      | [operations.LinkedinAccountProxy](../../models/operations/linkedin-account-proxy.md)         | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `apiKey`                                                                                     | [operations.ApiKey](../../models/operations/api-key.md)                                      | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `createdAt`                                                                                  | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |