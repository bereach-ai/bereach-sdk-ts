# ContextDeleteRequest

## Example Usage

```typescript
import { ContextDeleteRequest } from "bereach/models/operations";

let value: ContextDeleteRequest = {
  type: "<value>",
};
```

## Fields

| Field                      | Type                       | Required                   | Description                |
| -------------------------- | -------------------------- | -------------------------- | -------------------------- |
| `type`                     | *string*                   | :heavy_check_mark:         | Context type to delete     |
| `scope`                    | *string*                   | :heavy_minus_sign:         | Scope (defaults to "user") |