# ContextListEntry

## Example Usage

```typescript
import { ContextListEntry } from "bereach/models/operations";

let value: ContextListEntry = {
  id: "<id>",
  type: "<value>",
  label: "<value>",
  content: "<value>",
  scope: "<value>",
  updatedAt: "1735619611212",
};
```

## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `id`                                                                  | *string*                                                              | :heavy_check_mark:                                                    | Unique entry ID                                                       |
| `type`                                                                | *string*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `label`                                                               | *string*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `content`                                                             | *string*                                                              | :heavy_check_mark:                                                    | Full content (present when fullContent=true) or a 200-char preview    |
| `contentPreview`                                                      | *string*                                                              | :heavy_minus_sign:                                                    | First 200 chars of content: present when fullContent is not requested |
| `scope`                                                               | *string*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `updatedAt`                                                           | *string*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |