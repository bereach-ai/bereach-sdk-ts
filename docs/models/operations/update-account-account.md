# UpdateAccountAccount

## Example Usage

```typescript
import { UpdateAccountAccount } from "bereach/models/operations";

let value: UpdateAccountAccount = {
  id: "<id>",
  label: "<value>",
  isDefault: true,
  linkedinProfileId: "<id>",
  linkedinName: null,
  headline: null,
  profilePic: "<value>",
  isValid: true,
  isActive: false,
  proxyConfig: null,
};
```

## Fields

| Field                                                                                                          | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                           | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `label`                                                                                                        | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `isDefault`                                                                                                    | *boolean*                                                                                                      | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `linkedinProfileId`                                                                                            | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `linkedinName`                                                                                                 | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `headline`                                                                                                     | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `profilePic`                                                                                                   | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `isValid`                                                                                                      | *boolean*                                                                                                      | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `isActive`                                                                                                     | *boolean*                                                                                                      | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `proxyConfig`                                                                                                  | [operations.UpdateAccountProxyConfigResponse](../../models/operations/update-account-proxy-config-response.md) | :heavy_check_mark:                                                                                             | N/A                                                                                                            |