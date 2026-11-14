# PublicCompanyInternalServerError

The server encountered a situation it does not know how to handle. The body is the flat `{ error: "<text>" }` form, with `code` when the answer carries one; a few answers use the envelope.


## Supported Types

### `errors.ResponseBodyInternalServerErrorError1`

```typescript
const value: errors.ResponseBodyInternalServerErrorError1 = {
  error: "<value>",
};
```

### `errors.ResponseBodyInternalServerErrorError2`

```typescript
const value: errors.ResponseBodyInternalServerErrorError2 = {
  error: {
    code: "<value>",
    message: "<value>",
  },
};
```

