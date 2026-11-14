# PublicFindCompaniesNotApplied

## Example Usage

```typescript
import { PublicFindCompaniesNotApplied } from "bereach/models/operations";

let value: PublicFindCompaniesNotApplied = {
  reason: "saved-target",
};
```

## Fields

| Field                                                                                                                 | Type                                                                                                                  | Required                                                                                                              | Description                                                                                                           |
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `said`                                                                                                                | *string*                                                                                                              | :heavy_minus_sign:                                                                                                    | N/A                                                                                                                   |
| `industries`                                                                                                          | *string*[]                                                                                                            | :heavy_minus_sign:                                                                                                    | N/A                                                                                                                   |
| `named`                                                                                                               | *string*                                                                                                              | :heavy_minus_sign:                                                                                                    | N/A                                                                                                                   |
| `reason`                                                                                                              | [operations.PublicFindCompaniesNotAppliedReason](../../models/operations/public-find-companies-not-applied-reason.md) | :heavy_check_mark:                                                                                                    | Why it was taken out: it came from the saved target rather than the ask, or the request did not ask for it.           |