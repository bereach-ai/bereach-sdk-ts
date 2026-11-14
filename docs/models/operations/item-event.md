# ItemEvent

The event this company was read in, as it was returned. Null when no known event id was given.

## Example Usage

```typescript
import { ItemEvent } from "bereach/models/operations";

let value: ItemEvent = {
  id: "<id>",
  title: "<value>",
  date: "2024-07-29",
  url: "https://sick-shadowbox.net",
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `id`                                                                 | *string*                                                             | :heavy_check_mark:                                                   | N/A                                                                  |
| `title`                                                              | *string*                                                             | :heavy_check_mark:                                                   | N/A                                                                  |
| `date`                                                               | *string*                                                             | :heavy_check_mark:                                                   | When the event was published, YYYY-MM-DD. Null when it is not known. |
| `url`                                                                | *string*                                                             | :heavy_check_mark:                                                   | The source page.                                                     |