# GetOwnPostsRequest

## Example Usage

```typescript
import { GetOwnPostsRequest } from "bereach/models/operations";

let value: GetOwnPostsRequest = {};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `count`                                                                                                  | *number*                                                                                                 | :heavy_minus_sign:                                                                                       | Number of posts to fetch (default 20, max 100).                                                          |
| `start`                                                                                                  | *number*                                                                                                 | :heavy_minus_sign:                                                                                       | First page only. A start above 0 without paginationToken is refused: this feed pages by paginationToken. |
| `paginationToken`                                                                                        | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | The next page. Take it from the previous response; it is the only cursor this feed honours.              |
| `profileUrl`                                                                                             | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | Your own profile address, when it is not on file yet.                                                    |