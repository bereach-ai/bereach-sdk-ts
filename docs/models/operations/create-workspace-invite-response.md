# CreateWorkspaceInviteResponse

Invite created or listed


## Supported Types

### `operations.CreateWorkspaceInviteResponseBody1`

```typescript
const value: operations.CreateWorkspaceInviteResponseBody1 = {
  success: true,
  invite: {
    id: "<id>",
    email: "Briana.Renner@yahoo.com",
    name: "<value>",
    code: "<value>",
    maxUses: 113200,
    useCount: 348933,
    expiresAt: "1744363330649",
    createdAt: "1722545149857",
  },
  creditsUsed: 538260,
  retryAfter: 715490,
};
```

### `operations.CreateWorkspaceInviteResponseBody2`

```typescript
const value: operations.CreateWorkspaceInviteResponseBody2 = {
  success: true,
  invites: [
    {
      id: "<id>",
      email: "Marlon49@gmail.com",
      name: "<value>",
      code: "<value>",
      maxUses: 511240,
      useCount: 257969,
      expiresAt: "1747732612764",
      createdAt: "1719599439104",
    },
  ],
  workspace: {
    tier: "<value>",
    proSeatsIncluded: 455311,
    proSeatsUsed: 101401,
  },
  creditsUsed: 396869,
  retryAfter: 115536,
};
```

