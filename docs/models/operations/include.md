# Include

The parts to read, every one on by default; set a part false to leave it out.

## Example Usage

```typescript
import { Include } from "bereach/models/operations";

let value: Include = {};
```

## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `profile`                                                    | *boolean*                                                    | :heavy_minus_sign:                                           | N/A                                                          |
| `posts`                                                      | *boolean*                                                    | :heavy_minus_sign:                                           | N/A                                                          |
| `comments`                                                   | *boolean*                                                    | :heavy_minus_sign:                                           | Their recent reactions and comments on other people's posts. |
| `company`                                                    | *boolean*                                                    | :heavy_minus_sign:                                           | N/A                                                          |
| `signals`                                                    | *boolean*                                                    | :heavy_minus_sign:                                           | N/A                                                          |
| `history`                                                    | *boolean*                                                    | :heavy_minus_sign:                                           | The conversation with them.                                  |