# EventsFeedResponse

Events

## Example Usage

```typescript
import { EventsFeedResponse } from "bereach/models/operations";

let value: EventsFeedResponse = {
  events: [],
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `events`                                                                     | [operations.EventsFeedEvent](../../models/operations/events-feed-event.md)[] | :heavy_check_mark:                                                           | N/A                                                                          |
| `cursor`                                                                     | *number*                                                                     | :heavy_minus_sign:                                                           | Timestamp of most recent event (pass as 'since' for next poll)               |