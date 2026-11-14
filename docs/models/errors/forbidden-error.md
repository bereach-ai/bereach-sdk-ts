# ForbiddenError

The caller is authenticated but not allowed. Read error.code: subscription_required (API key or connector with no plan, running trial or money added, or whose trial was cancelled; error.message says how to turn it back on), free_draft_limit (a free-plan limit was reached), sales_nav_seat_inactive (no active Sales Navigator seat), or forbidden (not permitted).

## Example Usage

```typescript
import { ForbiddenError } from "bereach/models/errors";

// No examples available for this model
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `success`                                                                                               | *false*                                                                                                 | :heavy_minus_sign:                                                                                      | N/A                                                                                                     |
| `error`                                                                                                 | [operations.CollectEngagersForbiddenError](../../models/operations/collect-engagers-forbidden-error.md) | :heavy_check_mark:                                                                                      | N/A                                                                                                     |