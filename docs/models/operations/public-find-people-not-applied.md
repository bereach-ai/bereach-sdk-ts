# PublicFindPeopleNotApplied

## Example Usage

```typescript
import { PublicFindPeopleNotApplied } from "bereach/models/operations";

let value: PublicFindPeopleNotApplied = {
  reason: "saved-target",
};
```

## Fields

| Field                                                                                                           | Type                                                                                                            | Required                                                                                                        | Description                                                                                                     |
| --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| `said`                                                                                                          | *string*                                                                                                        | :heavy_minus_sign:                                                                                              | N/A                                                                                                             |
| `industries`                                                                                                    | *string*[]                                                                                                      | :heavy_minus_sign:                                                                                              | N/A                                                                                                             |
| `named`                                                                                                         | *string*                                                                                                        | :heavy_minus_sign:                                                                                              | N/A                                                                                                             |
| `reason`                                                                                                        | [operations.PublicFindPeopleNotAppliedReason](../../models/operations/public-find-people-not-applied-reason.md) | :heavy_check_mark:                                                                                              | Why it was taken out: it came from the saved target rather than the ask, or the request did not ask for it.     |