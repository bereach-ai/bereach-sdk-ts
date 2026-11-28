# ContactsUpsertResults

## Example Usage

```typescript
import { ContactsUpsertResults } from "bereach/models/operations";

let value: ContactsUpsertResults = {
  created: 94917,
  updated: 204733,
  skipped: 142139,
  errors: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
};
```

## Fields

| Field                                                                                   | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `created`                                                                               | *number*                                                                                | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `updated`                                                                               | *number*                                                                                | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `skipped`                                                                               | *number*                                                                                | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `errors`                                                                                | *string*[]                                                                              | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `bucketed`                                                                              | *number*                                                                                | :heavy_minus_sign:                                                                      | Rows left out because their URL carried no resolvable identity. Not counted in skipped. |