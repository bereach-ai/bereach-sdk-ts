# UpdateAccountRequest

## Example Usage

```typescript
import { UpdateAccountRequest } from "bereach/models/operations";

let value: UpdateAccountRequest = {
  accountId: "<id>",
};
```

## Fields

| Field                                                                                                                               | Type                                                                                                                                | Required                                                                                                                            | Description                                                                                                                         |
| ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| `accountId`                                                                                                                         | *string*                                                                                                                            | :heavy_check_mark:                                                                                                                  | ID of the LinkedIn account to update.                                                                                               |
| `label`                                                                                                                             | *string*                                                                                                                            | :heavy_minus_sign:                                                                                                                  | User-facing label (e.g. 'Personal', 'Company SDR').                                                                                 |
| `isDefault`                                                                                                                         | *boolean*                                                                                                                           | :heavy_minus_sign:                                                                                                                  | Set as the default account. Clears default from other accounts.                                                                     |
| `isActive`                                                                                                                          | *boolean*                                                                                                                           | :heavy_minus_sign:                                                                                                                  | Turn this LinkedIn account on or off. Turning it off pauses its connection requests and messages; it stays connected until removed. |
| `proxyConfig`                                                                                                                       | [operations.ProxyConfigRequest](../../models/operations/proxy-config-request.md)                                                    | :heavy_minus_sign:                                                                                                                  | Proxy config. Null = disable proxy. Object = enable with mode.                                                                      |