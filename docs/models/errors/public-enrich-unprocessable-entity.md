# PublicEnrichUnprocessableEntity

The request was well-formed but was unable to be followed due to semantic errors. The body is the flat `{ error: "<text>" }` form, with `code` when the answer carries one; a few answers use the envelope.


## Supported Types

### `errors.ResponseBodyUnprocessableEntityError1`

```typescript
const value: errors.ResponseBodyUnprocessableEntityError1 = {
  error: "<value>",
};
```

### `errors.ResponseBodyUnprocessableEntityError2`

```typescript
const value: errors.ResponseBodyUnprocessableEntityError2 = {
  error: {
    code: "<value>",
    message: "<value>",
  },
};
```

