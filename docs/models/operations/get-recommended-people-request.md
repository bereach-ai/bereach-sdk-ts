# GetRecommendedPeopleRequest

## Example Usage

```typescript
import { GetRecommendedPeopleRequest } from "bereach/models/operations";

let value: GetRecommendedPeopleRequest = {};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `limit`                                                                                                   | *number*                                                                                                  | :heavy_minus_sign:                                                                                        | How many people, up to 96 (24 by default), asked once: fewer can come back, and unresolved says how many. |