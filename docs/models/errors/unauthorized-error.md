# UnauthorizedError

Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. NOTE: 401 is also returned with code "linkedin_not_connected" on an endpoint that acts from your account (invitations, messages, your own network or inbox) when the caller IS authenticated but has no connected LinkedIn account: connect LinkedIn (not re-authenticate) to continue. Every other read never returns it.

## Example Usage

```typescript
import { UnauthorizedError } from "bereach/models/errors";

// No examples available for this model
```

## Fields

| Field                                                                                                         | Type                                                                                                          | Required                                                                                                      | Description                                                                                                   |
| ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                     | *false*                                                                                                       | :heavy_minus_sign:                                                                                            | N/A                                                                                                           |
| `error`                                                                                                       | [operations.CollectEngagersUnauthorizedError](../../models/operations/collect-engagers-unauthorized-error.md) | :heavy_check_mark:                                                                                            | N/A                                                                                                           |