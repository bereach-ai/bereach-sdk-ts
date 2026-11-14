# FindConversationRequest

## Example Usage

```typescript
import { FindConversationRequest } from "bereach/models/operations";

let value: FindConversationRequest = {
  profile: "<value>",
};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `profile`                                                                     | *string*                                                                      | :heavy_check_mark:                                                            | Accepts full profile URLs, vanity names (e.g. marie-sandre), or profile URNs. |
| `includeMessages`                                                             | *boolean*                                                                     | :heavy_minus_sign:                                                            | If true, also return the conversation's recent messages.                      |