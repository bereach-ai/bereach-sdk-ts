# AcceptInvitationRequest

## Example Usage

```typescript
import { AcceptInvitationRequest } from "bereach/models/operations";

let value: AcceptInvitationRequest = {
  invitationId: "<id>",
  sharedSecret: "<value>",
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `invitationId`                                                                                               | *string*                                                                                                     | :heavy_check_mark:                                                                                           | Invitation ID (from the list invitations endpoint)                                                           |
| `sharedSecret`                                                                                               | *string*                                                                                                     | :heavy_check_mark:                                                                                           | Shared secret / validation token (from the list invitations endpoint)                                        |
| `senderProfileId`                                                                                            | *string*                                                                                                     | :heavy_minus_sign:                                                                                           | Sender's profile ID (from the list invitations endpoint, e.g. 'ACoAAB1234...'). Recommended for reliability. |
| `firstName`                                                                                                  | *string*                                                                                                     | :heavy_minus_sign:                                                                                           | Sender's first name (from the list invitations endpoint). Recommended for reliability.                       |
| `lastName`                                                                                                   | *string*                                                                                                     | :heavy_minus_sign:                                                                                           | Sender's last name (from the list invitations endpoint). Recommended for reliability.                        |