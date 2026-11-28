# GetConnectionsConnection

## Example Usage

```typescript
import { GetConnectionsConnection } from "bereach/models/operations";

let value: GetConnectionsConnection = {
  name: "<value>",
  headline: null,
  profileUrl: "https://smart-wedding.net/",
  profileUrn: "<value>",
  publicIdentifier: "<value>",
  profilePicture: "<value>",
  connectedAt: "<value>",
};
```

## Fields

| Field                                             | Type                                              | Required                                          | Description                                       |
| ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- |
| `name`                                            | *string*                                          | :heavy_check_mark:                                | N/A                                               |
| `headline`                                        | *string*                                          | :heavy_check_mark:                                | N/A                                               |
| `profileUrl`                                      | *string*                                          | :heavy_check_mark:                                | N/A                                               |
| `profileUrn`                                      | *string*                                          | :heavy_check_mark:                                | N/A                                               |
| `publicIdentifier`                                | *string*                                          | :heavy_check_mark:                                | N/A                                               |
| `profilePicture`                                  | *string*                                          | :heavy_check_mark:                                | Profile picture URL                               |
| `connectedAt`                                     | *operations.ConnectedAt*                          | :heavy_check_mark:                                | Connection date (Unix timestamp ms or ISO string) |