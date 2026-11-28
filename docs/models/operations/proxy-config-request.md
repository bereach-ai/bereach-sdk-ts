# ProxyConfigRequest

Proxy config. Null = disable proxy. Object = enable with mode.

## Example Usage

```typescript
import { ProxyConfigRequest } from "bereach/models/operations";

let value: ProxyConfigRequest = {
  mode: "residential",
  country: "Dominica",
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `mode`                                                                         | [operations.UpdateAccountMode](../../models/operations/update-account-mode.md) | :heavy_check_mark:                                                             | N/A                                                                            |
| `country`                                                                      | *string*                                                                       | :heavy_check_mark:                                                             | ISO 3166-1 alpha-2 country code.                                               |
| `city`                                                                         | *string*                                                                       | :heavy_minus_sign:                                                             | City for geo-targeting.                                                        |
| `rotationHours`                                                                | *number*                                                                       | :heavy_minus_sign:                                                             | Sticky IP rotation in hours (default 1).                                       |