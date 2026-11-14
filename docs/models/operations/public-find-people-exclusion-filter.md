# PublicFindPeopleExclusionFilter

What the person's exclusions did, present whenever the ask carried any.

## Example Usage

```typescript
import { PublicFindPeopleExclusionFilter } from "bereach/models/operations";

let value: PublicFindPeopleExclusionFilter = {
  kinds: [
    {
      said: "<id>",
      industries: [
        "<value 1>",
        "<value 2>",
        "<value 3>",
      ],
      leftOut: 8775.56,
    },
  ],
  named: {
    count: 2456.69,
    leftOut: 1681.18,
    skippedBeforeSearch: 3319.15,
  },
  kindUnknown: 598.31,
  checkFailed: 956.81,
  applied: false,
  keepsNobody: false,
};
```

## Fields

| Field                                                                                                               | Type                                                                                                                | Required                                                                                                            | Description                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `kinds`                                                                                                             | [operations.PublicFindPeopleKindNamedCompany](../../models/operations/public-find-people-kind-named-company.md)[]   | :heavy_check_mark:                                                                                                  | Each kind applied, with how many it left out.                                                                       |
| `named`                                                                                                             | [operations.PublicFindPeopleNamed](../../models/operations/public-find-people-named.md)                             | :heavy_check_mark:                                                                                                  | The named companies applied.                                                                                        |
| `kindUnknown`                                                                                                       | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | Kept although their company's industry is not known.                                                                |
| `checkFailed`                                                                                                       | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | Kept although their company could not be checked just now; asking again checks them.                                |
| `applied`                                                                                                           | *boolean*                                                                                                           | :heavy_check_mark:                                                                                                  | False when nothing was checked because the search names its answer.                                                 |
| `reason`                                                                                                            | [operations.PublicFindPeopleReasonNamedCompany](../../models/operations/public-find-people-reason-named-company.md) | :heavy_minus_sign:                                                                                                  | Why it was not applied: the search names its answer.                                                                |
| `keepsNobody`                                                                                                       | *boolean*                                                                                                           | :heavy_check_mark:                                                                                                  | The search stopped after two searches in a row kept nobody.                                                         |
| `notApplied`                                                                                                        | [operations.PublicFindPeopleNotApplied](../../models/operations/public-find-people-not-applied.md)[]                | :heavy_minus_sign:                                                                                                  | Exclusions taken out before the search because the person did not ask for them.                                     |