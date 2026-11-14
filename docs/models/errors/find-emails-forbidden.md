# FindEmailsForbidden

The caller is authenticated but not allowed. Read code: subscription_required (API key or connector with no plan, running trial or money added, or whose trial was cancelled; error.message says how to turn it back on), free_draft_limit (a free-plan limit was reached), sales_nav_seat_inactive (no active Sales Navigator seat), or forbidden (not permitted). The body is the flat `{ error: "<text>" }` form, with `code` when the answer carries one; a few answers use the envelope.


## Supported Types

### `errors.ResponseBodyForbiddenError1`

```typescript
const value: errors.ResponseBodyForbiddenError1 = {
  error: "<value>",
};
```

### `errors.ResponseBodyForbiddenError2`

```typescript
const value: errors.ResponseBodyForbiddenError2 = {
  error: {
    code: "<value>",
    message: "<value>",
  },
};
```

