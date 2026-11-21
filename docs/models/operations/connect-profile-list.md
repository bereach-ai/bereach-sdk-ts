# ConnectProfileList

Only present on a dryRun response: which list this call would actually target, and its real current state.

## Example Usage

```typescript
import { ConnectProfileList } from "bereach/models/operations";

let value: ConnectProfileList = {
  name: "<value>",
  isNew: true,
  totalMembers: 1340.32,
};
```

## Fields

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `name`                                                                      | *string*                                                                    | :heavy_check_mark:                                                          | N/A                                                                         |
| `isNew`                                                                     | *boolean*                                                                   | :heavy_check_mark:                                                          | True if this exact list does not exist yet and a real call would create it. |
| `totalMembers`                                                              | *number*                                                                    | :heavy_check_mark:                                                          | How many people are already in this list, before this call.                 |