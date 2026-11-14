# StatusRequest

Default 'draft'. 'scheduled' means approve at once: the message is put in line and goes out once the person is connected, at the account's pace.

## Example Usage

```typescript
import { StatusRequest } from "bereach/models/operations";

let value: StatusRequest = "draft";
```

## Values

```typescript
"draft" | "scheduled"
```