# PublicFindCompaniesConflict

The request conflicts with the current state of the server. The body is the flat `{ error: "<text>" }` form, with `code` when the answer carries one; a few answers use the envelope.


## Supported Types

### `errors.ResponseBodyConflictError1`

```typescript
const value: errors.ResponseBodyConflictError1 = {
  error: "<value>",
};
```

### `errors.ResponseBodyConflictError2`

```typescript
const value: errors.ResponseBodyConflictError2 = {
  error: {
    code: "<value>",
    message: "<value>",
  },
};
```

