# RoleStart

What the months-in-role window did, present whenever the ask carried one.

## Example Usage

```typescript
import { RoleStart } from "bereach/models/operations";

let value: RoleStart = {
  min: 6043.91,
  max: 2408.86,
  kept: 2935.49,
  outside: 3802.91,
  undated: 4190.73,
  applied: false,
};
```

## Fields

| Field                                                                                                               | Type                                                                                                                | Required                                                                                                            | Description                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `min`                                                                                                               | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `max`                                                                                                               | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `kept`                                                                                                              | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | People kept whose current role started inside the window.                                                           |
| `outside`                                                                                                           | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | On-topic people left out because their current role started outside it.                                             |
| `undated`                                                                                                           | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | On-topic people left out because their current role has no start date.                                              |
| `applied`                                                                                                           | *boolean*                                                                                                           | :heavy_check_mark:                                                                                                  | False when this search names its answer and shows every match however long they have held their role.               |
| `reason`                                                                                                            | [operations.PublicFindPeopleReasonNamedCompany](../../models/operations/public-find-people-reason-named-company.md) | :heavy_minus_sign:                                                                                                  | N/A                                                                                                                 |