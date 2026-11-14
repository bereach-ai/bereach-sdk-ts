# RunSearchesNotFound

The server cannot find the requested resource. The body is the flat `{ error: "<text>" }` form, with `code` when the answer carries one; a few answers use the envelope.


## Supported Types

### `errors.ResponseBodyNotFoundError1`

```typescript
const value: errors.ResponseBodyNotFoundError1 = {
  error: "<value>",
};
```

### `errors.ResponseBodyNotFoundError2`

```typescript
const value: errors.ResponseBodyNotFoundError2 = {
  error: {
    code: "<value>",
    message: "<value>",
  },
};
```

