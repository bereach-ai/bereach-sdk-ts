# PublicFindPeopleEmployerFacts

How many people in this answer carry their employer's facts, and why the others do not.

## Example Usage

```typescript
import { PublicFindPeopleEmployerFacts } from "bereach/models/operations";

let value: PublicFindPeopleEmployerFacts = {
  withFacts: 197173,
  noRecord: 923638,
  failed: 158116,
  notChecked: 617255,
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `withFacts`                                                                                      | *number*                                                                                         | :heavy_check_mark:                                                                               | People in this answer whose row carries their employer's facts.                                  |
| `noRecord`                                                                                       | *number*                                                                                         | :heavy_check_mark:                                                                               | People whose employer has no company record: their rows carry no employer facts.                 |
| `failed`                                                                                         | *number*                                                                                         | :heavy_check_mark:                                                                               | People whose employer could not be checked just now; asking again checks them.                   |
| `notChecked`                                                                                     | *number*                                                                                         | :heavy_check_mark:                                                                               | People whose employer's record was not read for this answer: their rows carry no employer facts. |