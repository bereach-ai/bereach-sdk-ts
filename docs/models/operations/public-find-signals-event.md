# PublicFindSignalsEvent

## Example Usage

```typescript
import { PublicFindSignalsEvent } from "bereach/models/operations";

let value: PublicFindSignalsEvent = {
  id: "<id>",
  title: "<value>",
  date: "2024-07-28",
  url: "https://innocent-apparatus.biz",
  text: "<value>",
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `id`                                                                 | *string*                                                             | :heavy_check_mark:                                                   | N/A                                                                  |
| `title`                                                              | *string*                                                             | :heavy_check_mark:                                                   | N/A                                                                  |
| `date`                                                               | *string*                                                             | :heavy_check_mark:                                                   | When the event was published, YYYY-MM-DD. Null when it is not known. |
| `url`                                                                | *string*                                                             | :heavy_check_mark:                                                   | The source page.                                                     |
| `text`                                                               | *string*                                                             | :heavy_check_mark:                                                   | The opening of the source page.                                      |