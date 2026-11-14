# PublicFindCompaniesKindNamedCompany

## Example Usage

```typescript
import { PublicFindCompaniesKindNamedCompany } from "bereach/models/operations";

let value: PublicFindCompaniesKindNamedCompany = {
  said: "<id>",
  industries: [
    "<value 1>",
    "<value 2>",
  ],
  leftOut: 3709.84,
};
```

## Fields

| Field                                       | Type                                        | Required                                    | Description                                 |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `said`                                      | *string*                                    | :heavy_check_mark:                          | The person's words for this kind.           |
| `industries`                                | *string*[]                                  | :heavy_check_mark:                          | The industry names applied.                 |
| `leftOut`                                   | *number*                                    | :heavy_check_mark:                          | People or companies left out for this kind. |