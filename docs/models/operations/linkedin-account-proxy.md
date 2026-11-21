# LinkedinAccountProxy

## Example Usage

```typescript
import { LinkedinAccountProxy } from "bereach/models/operations";

let value: LinkedinAccountProxy = {
  enabled: false,
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `enabled`                                                                  | *boolean*                                                                  | :heavy_check_mark:                                                         | N/A                                                                        |
| `mode`                                                                     | *string*                                                                   | :heavy_minus_sign:                                                         | Connection mode for the account.                                           |
| `country`                                                                  | *string*                                                                   | :heavy_minus_sign:                                                         | Country the account connects from, ISO alpha-2, uppercase on this surface. |
| `rotationHours`                                                            | *number*                                                                   | :heavy_minus_sign:                                                         | How many hours the connection location is kept before it changes.          |