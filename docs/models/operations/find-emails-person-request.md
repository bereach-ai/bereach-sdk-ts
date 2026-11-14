# FindEmailsPersonRequest

## Example Usage

```typescript
import { FindEmailsPersonRequest } from "bereach/models/operations";

let value: FindEmailsPersonRequest = {
  profileUrl: "https://good-natured-possession.org",
};
```

## Fields

| Field                                       | Type                                        | Required                                    | Description                                 |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `profileUrl`                                | *string*                                    | :heavy_check_mark:                          | The person's profile address.               |
| `name`                                      | *string*                                    | :heavy_minus_sign:                          | The person's full name.                     |
| `domain`                                    | *string*                                    | :heavy_minus_sign:                          | Their current employer's website or domain. |