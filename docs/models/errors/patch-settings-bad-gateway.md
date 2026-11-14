# PatchSettingsBadGateway

An upstream service returned an error. Retry after a few seconds. The body is the flat `{ error: "<text>" }` form, with `code` when the answer carries one; a few answers use the envelope.


## Supported Types

### `errors.ResponseBodyBadGatewayError1`

```typescript
const value: errors.ResponseBodyBadGatewayError1 = {
  error: "<value>",
};
```

### `errors.ResponseBodyBadGatewayError2`

```typescript
const value: errors.ResponseBodyBadGatewayError2 = {
  error: {
    code: "<value>",
    message: "<value>",
  },
};
```

