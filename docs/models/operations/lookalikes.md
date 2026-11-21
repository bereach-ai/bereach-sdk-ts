# Lookalikes

A search for people at companies like the ones in the list: what it started from and how it ended. The companies searched are namedCompanies.

## Example Usage

```typescript
import { Lookalikes } from "bereach/models/operations";

let value: Lookalikes = {
  outcome: "nobody-in-roles",
  examples: [
    "<value 1>",
    "<value 2>",
  ],
  examplesNotFound: [
    "<value 1>",
    "<value 2>",
  ],
  examplesFailed: [
    "<value 1>",
  ],
  roles: [
    "<value 1>",
  ],
  rolesFromList: false,
  waiting: 423734,
  known: 269824,
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `outcome`                                                                                   | [operations.PublicFindPeopleOutcome](../../models/operations/public-find-people-outcome.md) | :heavy_check_mark:                                                                          | How a search for people at companies like the ones in the list ended.                       |
| `examples`                                                                                  | *string*[]                                                                                  | :heavy_check_mark:                                                                          | The list's companies whose look-alikes were searched.                                       |
| `examplesNotFound`                                                                          | *string*[]                                                                                  | :heavy_check_mark:                                                                          | List companies no company carries exactly by name.                                          |
| `examplesFailed`                                                                            | *string*[]                                                                                  | :heavy_check_mark:                                                                          | List companies that could not be looked up just now.                                        |
| `roles`                                                                                     | *string*[]                                                                                  | :heavy_check_mark:                                                                          | The roles looked for.                                                                       |
| `rolesFromList`                                                                             | *boolean*                                                                                   | :heavy_check_mark:                                                                          | True when the roles are the ones most held in the list, not the ones asked.                 |
| `waiting`                                                                                   | *number*                                                                                    | :heavy_check_mark:                                                                          | Companies like them found and left for the next search.                                     |
| `known`                                                                                     | *number*                                                                                    | :heavy_check_mark:                                                                          | Companies skipped because they were in the list or searched before.                         |