# PublicFindPeopleKindNamedCompany

## Example Usage

```typescript
import { PublicFindPeopleKindNamedCompany } from "bereach/models/operations";

let value: PublicFindPeopleKindNamedCompany = {
  said: "<id>",
  industries: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
  leftOut: 6514.19,
};
```

## Fields

| Field                                       | Type                                        | Required                                    | Description                                 |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `said`                                      | *string*                                    | :heavy_check_mark:                          | The person's words for this kind.           |
| `industries`                                | *string*[]                                  | :heavy_check_mark:                          | The industry names applied.                 |
| `leftOut`                                   | *number*                                    | :heavy_check_mark:                          | People or companies left out for this kind. |