# PublicFindCompaniesIgnoredField

## Example Usage

```typescript
import { PublicFindCompaniesIgnoredField } from "bereach/models/operations";

let value: PublicFindCompaniesIgnoredField = {
  field: "<value>",
};
```

## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `field`                                                       | *string*                                                      | :heavy_check_mark:                                            | The field as sent, under filters or at the top level.         |
| `didYouMean`                                                  | *string*                                                      | :heavy_minus_sign:                                            | The field that does this, when the name is a known near miss. |