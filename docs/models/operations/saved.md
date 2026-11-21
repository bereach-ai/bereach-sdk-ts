# Saved

What the save choice actually did, so claims about saving cite this rather than the request that was sent.

## Example Usage

```typescript
import { Saved } from "bereach/models/operations";

let value: Saved = {
  count: 937717,
};
```

## Fields

| Field                                                                                                                                                                                                          | Type                                                                                                                                                                                                           | Required                                                                                                                                                                                                       | Description                                                                                                                                                                                                    |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `count`                                                                                                                                                                                                        | *number*                                                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                                                             | People written to the contact list by THIS call.                                                                                                                                                               |
| `decide`                                                                                                                                                                                                       | *boolean*                                                                                                                                                                                                      | :heavy_minus_sign:                                                                                                                                                                                             | The caller was not sure whether to keep these people, so nobody was written and the person is offered the choice on the result itself. Do not tell them anything was kept, and do not ask them again in words. |