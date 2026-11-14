# Ambiguity

## Example Usage

```typescript
import { Ambiguity } from "bereach/models/operations";

let value: Ambiguity = {
  name: "<value>",
  note: "<value>",
};
```

## Fields

| Field                                     | Type                                      | Required                                  | Description                               |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| `name`                                    | *string*                                  | :heavy_check_mark:                        | The organisation name that is ambiguous.  |
| `note`                                    | *string*                                  | :heavy_check_mark:                        | What to ask before trusting a single row. |