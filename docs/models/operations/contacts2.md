# Contacts2

Identity and list stage only. No profile blob, no campaign membership, no timestamps.

## Example Usage

```typescript
import { Contacts2 } from "bereach/models/operations";

let value: Contacts2 = {
  id: "<id>",
  linkedinUrl: "https://ironclad-metal.net/",
  name: "<value>",
  lifecycleStage: "<value>",
  outreachStatus: "<value>",
  doNotContact: false,
};
```

## Fields

| Field                                             | Type                                              | Required                                          | Description                                       |
| ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- |
| `id`                                              | *string*                                          | :heavy_check_mark:                                | N/A                                               |
| `linkedinUrl`                                     | *string*                                          | :heavy_check_mark:                                | N/A                                               |
| `name`                                            | *string*                                          | :heavy_check_mark:                                | N/A                                               |
| `lifecycleStage`                                  | *string*                                          | :heavy_check_mark:                                | List stage; rejected means removed from the list. |
| `outreachStatus`                                  | *string*                                          | :heavy_check_mark:                                | N/A                                               |
| `doNotContact`                                    | *boolean*                                         | :heavy_check_mark:                                | N/A                                               |