# PatchSettingsGone

The requested content has been permanently deleted from the server. The body is the flat `{ error: "<text>" }` form, with `code` when the answer carries one; a few answers use the envelope.


## Supported Types

### `errors.ResponseBodyGoneError1`

```typescript
const value: errors.ResponseBodyGoneError1 = {
  error: "<value>",
};
```

### `errors.ResponseBodyGoneError2`

```typescript
const value: errors.ResponseBodyGoneError2 = {
  error: {
    code: "<value>",
    message: "<value>",
  },
};
```

