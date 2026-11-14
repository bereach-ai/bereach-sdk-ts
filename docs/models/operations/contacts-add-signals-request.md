# ContactsAddSignalsRequest

## Example Usage

```typescript
import { ContactsAddSignalsRequest } from "bereach/models/operations";

let value: ContactsAddSignalsRequest = {
  campaignId: "<id>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `campaignId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | The list to read.                                                                             |
| `start`                                                                                       | *boolean*                                                                                     | :heavy_minus_sign:                                                                            | false reads where the last run stands and what a new one costs at most, without starting one. |