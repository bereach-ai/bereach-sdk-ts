# PublicFindPeopleNamed

The named companies applied.

## Example Usage

```typescript
import { PublicFindPeopleNamed } from "bereach/models/operations";

let value: PublicFindPeopleNamed = {
  count: 4997.64,
  leftOut: 8287.62,
  skippedBeforeSearch: 3937.74,
};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `count`                                                                         | *number*                                                                        | :heavy_check_mark:                                                              | Companies named.                                                                |
| `leftOut`                                                                       | *number*                                                                        | :heavy_check_mark:                                                              | People or companies left out because they are at, or are, a company named.      |
| `skippedBeforeSearch`                                                           | *number*                                                                        | :heavy_check_mark:                                                              | Companies named that this search was about to search inside and never searched. |