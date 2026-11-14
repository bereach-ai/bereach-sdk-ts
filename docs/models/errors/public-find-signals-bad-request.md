# PublicFindSignalsBadRequest

The server cannot or will not process the request due to something that is perceived to be a client error. The body is the flat `{ error: "<text>" }` form, with `code` when the answer carries one; a few answers use the envelope.


## Supported Types

### `errors.ResponseBodyBadRequestError1`

```typescript
const value: errors.ResponseBodyBadRequestError1 = {
  error: "<value>",
};
```

### `errors.ResponseBodyBadRequestError2`

```typescript
const value: errors.ResponseBodyBadRequestError2 = {
  error: {
    code: "<value>",
    message: "<value>",
  },
};
```

