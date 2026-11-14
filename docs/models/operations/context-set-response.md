# ContextSetResponse

Context saved, or removed


## Supported Types

### `operations.ContextSetResponseBody1`

```typescript
const value: operations.ContextSetResponseBody1 = {
  success: true,
  entry: {
    id: "<id>",
    type: "<value>",
    label: "<value>",
    content: "<value>",
    scope: "<value>",
    updatedAt: "1735627605473",
  },
  creditsUsed: 443677,
  retryAfter: 264509,
};
```

### `operations.ContextSetResponseBody2`

```typescript
const value: operations.ContextSetResponseBody2 = {
  success: true,
  removed: {
    type: "<value>",
    label: null,
    scope: "<value>",
  },
  unboundFrom: [],
  creditsUsed: 824563,
  retryAfter: 100745,
};
```

