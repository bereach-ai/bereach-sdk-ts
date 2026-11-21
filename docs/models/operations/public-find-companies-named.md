# PublicFindCompaniesNamed

The named companies applied.

## Example Usage

```typescript
import { PublicFindCompaniesNamed } from "bereach/models/operations";

let value: PublicFindCompaniesNamed = {
  count: 9886.96,
  leftOut: 9260.2,
  skippedBeforeSearch: 4722.81,
};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `count`                                                                         | *number*                                                                        | :heavy_check_mark:                                                              | Companies named.                                                                |
| `leftOut`                                                                       | *number*                                                                        | :heavy_check_mark:                                                              | People or companies left out because they are at, or are, a company named.      |
| `skippedBeforeSearch`                                                           | *number*                                                                        | :heavy_check_mark:                                                              | Companies named that this search was about to search inside and never searched. |