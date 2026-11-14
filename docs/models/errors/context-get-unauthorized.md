# ContextGetUnauthorized

Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. NOTE: 401 is also returned with code "linkedin_not_connected" on an endpoint that acts from your account (invitations, messages, your own network or inbox) when the caller IS authenticated but has no connected LinkedIn account: connect LinkedIn (not re-authenticate) to continue. Every other read never returns it. The body is the flat `{ error: "<text>" }` form, with `code` when the answer carries one; a few answers use the envelope.


## Supported Types

### `errors.ResponseBodyUnauthorizedError1`

```typescript
const value: errors.ResponseBodyUnauthorizedError1 = {
  error: "<value>",
};
```

### `errors.ResponseBodyUnauthorizedError2`

```typescript
const value: errors.ResponseBodyUnauthorizedError2 = {
  error: {
    code: "<value>",
    message: "<value>",
  },
};
```

