# InboxListRequest

## Example Usage

```typescript
import { InboxListRequest } from "bereach/models/operations";

let value: InboxListRequest = {};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `nextCursor`                                           | *string*                                               | :heavy_minus_sign:                                     | Pagination cursor from a previous response             |
| `count`                                                | *number*                                               | :heavy_minus_sign:                                     | Number of conversations to return (default 20, max 25) |