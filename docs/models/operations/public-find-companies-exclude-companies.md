# PublicFindCompaniesExcludeCompanies

Companies to leave out, by kind or by name; on a people search, the people who work there.

## Example Usage

```typescript
import { PublicFindCompaniesExcludeCompanies } from "bereach/models/operations";

let value: PublicFindCompaniesExcludeCompanies = {};
```

## Fields

| Field                                                                                                                           | Type                                                                                                                            | Required                                                                                                                        | Description                                                                                                                     |
| ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| `kinds`                                                                                                                         | [operations.PublicFindCompaniesExcludeCompaniesKind](../../models/operations/public-find-companies-exclude-companies-kind.md)[] | :heavy_minus_sign:                                                                                                              | Kinds of company to leave out.                                                                                                  |
| `named`                                                                                                                         | *string*[]                                                                                                                      | :heavy_minus_sign:                                                                                                              | Companies to leave out, by name.                                                                                                |