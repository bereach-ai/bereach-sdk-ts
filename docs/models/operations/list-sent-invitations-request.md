# ListSentInvitationsRequest

## Example Usage

```typescript
import { ListSentInvitationsRequest } from "bereach/models/operations";

let value: ListSentInvitationsRequest = {};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `start`                                                                                    | *number*                                                                                   | :heavy_minus_sign:                                                                         | Pagination offset                                                                          |
| `count`                                                                                    | *number*                                                                                   | :heavy_minus_sign:                                                                         | Number of invitations to return                                                            |
| `olderThanDays`                                                                            | *number*                                                                                   | :heavy_minus_sign:                                                                         | Only invitations sent at least this many days ago; start and count then page through those |
| `scanFrom`                                                                                 | *number*                                                                                   | :heavy_minus_sign:                                                                         | With olderThanDays: the previous answer's nextScanFrom, to read on where it stopped        |