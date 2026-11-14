# Update

Fields to update on all matching contacts

## Example Usage

```typescript
import { Update } from "bereach/models/operations";

let value: Update = {};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `lifecycleStage`                                                                                        | [operations.DiscardContactsLifecycleStage](../../models/operations/discard-contacts-lifecycle-stage.md) | :heavy_minus_sign:                                                                                      | A list change: rejected removes them from the list campaignId names, contact brings them back.          |
| `notes`                                                                                                 | *string*                                                                                                | :heavy_minus_sign:                                                                                      | A note kept on each person.                                                                             |
| `outreachStatus`                                                                                        | [operations.DiscardContactsOutreachStatus](../../models/operations/discard-contacts-outreach-status.md) | :heavy_minus_sign:                                                                                      | N/A                                                                                                     |
| `doNotContact`                                                                                          | *boolean*                                                                                               | :heavy_minus_sign:                                                                                      | True: never invite or message them.                                                                     |
| `tags`                                                                                                  | *operations.DiscardContactsTagsUnion*                                                                   | :heavy_minus_sign:                                                                                      | Tag operations: { add, remove } or { set }                                                              |