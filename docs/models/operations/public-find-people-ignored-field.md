# PublicFindPeopleIgnoredField

## Example Usage

```typescript
import { PublicFindPeopleIgnoredField } from "bereach/models/operations";

let value: PublicFindPeopleIgnoredField = {
  field: "<value>",
};
```

## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `field`                                                       | *string*                                                      | :heavy_check_mark:                                            | The field as sent, under filters or at the top level.         |
| `didYouMean`                                                  | *string*                                                      | :heavy_minus_sign:                                            | The field that does this, when the name is a known near miss. |