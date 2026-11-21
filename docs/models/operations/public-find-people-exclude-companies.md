# PublicFindPeopleExcludeCompanies

Companies to leave out, by kind or by name; on a people search, the people who work there.

## Example Usage

```typescript
import { PublicFindPeopleExcludeCompanies } from "bereach/models/operations";

let value: PublicFindPeopleExcludeCompanies = {};
```

## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `kinds`                                                       | [operations.KindList](../../models/operations/kind-list.md)[] | :heavy_minus_sign:                                            | Kinds of company to leave out.                                |
| `named`                                                       | *string*[]                                                    | :heavy_minus_sign:                                            | Companies to leave out, by name.                              |