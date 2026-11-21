# Coverage

What this ask has searched, and what it asked for but has not reached yet, over every call of it.

## Example Usage

```typescript
import { Coverage } from "bereach/models/operations";

let value: Coverage = {
  placesSearched: [
    "<value 1>",
    "<value 2>",
  ],
  placesNotReached: [
    "<value 1>",
  ],
  kindsSearched: [
    "<value 1>",
    "<value 2>",
  ],
  kindsNotReached: [],
  titlesSearched: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
  titlesNotReached: [],
};
```

## Fields

| Field                                                                                                                                                                                 | Type                                                                                                                                                                                  | Required                                                                                                                                                                              | Description                                                                                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `placesSearched`                                                                                                                                                                      | *string*[]                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                    | Places this ask has searched so far.                                                                                                                                                  |
| `placesNotReached`                                                                                                                                                                    | *string*[]                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                    | Places asked for that no search has reached yet.                                                                                                                                      |
| `kindsSearched`                                                                                                                                                                       | *string*[]                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                    | Kinds of company this ask has searched so far.                                                                                                                                        |
| `kindsNotReached`                                                                                                                                                                     | *string*[]                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                    | Kinds of company asked for that no search has reached yet; asking again with more reaches them.                                                                                       |
| `titlesSearched`                                                                                                                                                                      | *string*[]                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                    | Job titles this ask has searched so far.                                                                                                                                              |
| `titlesNotReached`                                                                                                                                                                    | *string*[]                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                    | Job titles asked for that no search has reached yet.                                                                                                                                  |
| `sentenceSearched`                                                                                                                                                                    | *string*                                                                                                                                                                              | :heavy_minus_sign:                                                                                                                                                                    | The words searched exactly as the person wrote them, when they were. A place, kind of company or job title those words name is reached by them and listed in none of the lists above. |