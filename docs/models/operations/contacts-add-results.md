# ContactsAddResults

## Example Usage

```typescript
import { ContactsAddResults } from "bereach/models/operations";

let value: ContactsAddResults = {
  created: 974501,
  skipped: 413995,
  errors: [
    "<value 1>",
  ],
};
```

## Fields

| Field                                                                                   | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `created`                                                                               | *number*                                                                                | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `skipped`                                                                               | *number*                                                                                | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `errors`                                                                                | *string*[]                                                                              | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `alreadyLinked`                                                                         | *number*                                                                                | :heavy_minus_sign:                                                                      | Of the skipped rows, the people who were already on this list.                          |
| `bucketed`                                                                              | *number*                                                                                | :heavy_minus_sign:                                                                      | Rows left out because their URL carried no resolvable identity. Not counted in skipped. |