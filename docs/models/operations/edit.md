# Edit


## Supported Types

### `operations.EditRemove`

```typescript
const value: operations.EditRemove = {
  op: "remove",
  field: "peopleWanted",
};
```

### `operations.EditPick`

```typescript
const value: operations.EditPick = {
  op: "pick",
  icp: "<value>",
  field: "kinds",
  value: "<value>",
};
```

### `operations.EditFirst`

```typescript
const value: operations.EditFirst = {
  op: "first",
  icp: "<value>",
};
```

### `operations.EditDrop`

```typescript
const value: operations.EditDrop = {
  op: "drop",
  icp: "<value>",
};
```

### `operations.EditMore`

```typescript
const value: operations.EditMore = {
  op: "more",
};
```

