# WorkspaceMember

## Example Usage

```typescript
import { WorkspaceMember } from "bereach/models/operations";

let value: WorkspaceMember = {
  id: "<id>",
  name: "<value>",
  email: "Major.Friesen@gmail.com",
  isOwner: true,
  role: "member",
};
```

## Fields

| Field                                              | Type                                               | Required                                           | Description                                        |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `id`                                               | *string*                                           | :heavy_check_mark:                                 | N/A                                                |
| `name`                                             | *string*                                           | :heavy_check_mark:                                 | N/A                                                |
| `email`                                            | *string*                                           | :heavy_check_mark:                                 | N/A                                                |
| `isOwner`                                          | *boolean*                                          | :heavy_check_mark:                                 | N/A                                                |
| `role`                                             | [operations.Role](../../models/operations/role.md) | :heavy_check_mark:                                 | N/A                                                |