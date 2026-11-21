# PublicFindSignalsServiceUnavailable

Capacity is temporarily exceeded. Retry after a few seconds. The body is the flat `{ error: "<text>" }` form, with `code` when the answer carries one; a few answers use the envelope.


## Supported Types

### `errors.ResponseBodyServiceUnavailableError1`

```typescript
const value: errors.ResponseBodyServiceUnavailableError1 = {
  error: "<value>",
};
```

### `errors.ResponseBodyServiceUnavailableError2`

```typescript
const value: errors.ResponseBodyServiceUnavailableError2 = {
  error: {
    code: "<value>",
    message: "<value>",
  },
};
```

