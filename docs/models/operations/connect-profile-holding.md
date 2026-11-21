# ConnectProfileHolding

Set when nothing went out because of this account's own schedule: it only sends during its own set hours, or it is inside the gap between two invitations. Nothing is wrong, nobody has to act, and the people named are in line. Say when they go, do not report a problem and do not call it a limit.

## Example Usage

```typescript
import { ConnectProfileHolding } from "bereach/models/operations";

let value: ConnectProfileHolding = {
  kind: "outside_window",
  message: "<value>",
  resumesAt: "<value>",
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `kind`                                                                           | [operations.ConnectProfileKind](../../models/operations/connect-profile-kind.md) | :heavy_check_mark:                                                               | N/A                                                                              |
| `message`                                                                        | *string*                                                                         | :heavy_check_mark:                                                               | A plain sentence explaining the wait, suitable to show as written                |
| `resumesAt`                                                                      | *string*                                                                         | :heavy_check_mark:                                                               | When sending resumes on its own                                                  |