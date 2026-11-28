# PublicFindCompaniesExclusionFilter

What the person's exclusions did, present whenever the ask carried any.

## Example Usage

```typescript
import { PublicFindCompaniesExclusionFilter } from "bereach/models/operations";

let value: PublicFindCompaniesExclusionFilter = {
  kinds: [],
  named: {
    count: 8445.63,
    leftOut: 8210.48,
    skippedBeforeSearch: 4315.61,
  },
  kindUnknown: 633,
  checkFailed: 1762.66,
  applied: true,
  keepsNobody: true,
};
```

## Fields

| Field                                                                                                                   | Type                                                                                                                    | Required                                                                                                                | Description                                                                                                             |
| ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `kinds`                                                                                                                 | [operations.PublicFindCompaniesKindNamedCompany](../../models/operations/public-find-companies-kind-named-company.md)[] | :heavy_check_mark:                                                                                                      | Each kind applied, with how many it left out.                                                                           |
| `named`                                                                                                                 | [operations.PublicFindCompaniesNamed](../../models/operations/public-find-companies-named.md)                           | :heavy_check_mark:                                                                                                      | The named companies applied.                                                                                            |
| `kindUnknown`                                                                                                           | *number*                                                                                                                | :heavy_check_mark:                                                                                                      | Kept although their company's industry is not known.                                                                    |
| `checkFailed`                                                                                                           | *number*                                                                                                                | :heavy_check_mark:                                                                                                      | Kept although their company could not be checked just now; asking again checks them.                                    |
| `applied`                                                                                                               | *boolean*                                                                                                               | :heavy_check_mark:                                                                                                      | False when nothing was checked because the search names its answer.                                                     |
| `reason`                                                                                                                | [operations.PublicFindCompaniesReason](../../models/operations/public-find-companies-reason.md)                         | :heavy_minus_sign:                                                                                                      | Why it was not applied: the search names its answer.                                                                    |
| `keepsNobody`                                                                                                           | *boolean*                                                                                                               | :heavy_check_mark:                                                                                                      | The search stopped after two searches in a row kept nobody.                                                             |
| `notApplied`                                                                                                            | [operations.PublicFindCompaniesNotApplied](../../models/operations/public-find-companies-not-applied.md)[]              | :heavy_minus_sign:                                                                                                      | Exclusions taken out before the search because the person did not ask for them.                                         |