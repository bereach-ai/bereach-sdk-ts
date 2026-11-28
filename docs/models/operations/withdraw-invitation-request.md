# WithdrawInvitationRequest

## Example Usage

```typescript
import { WithdrawInvitationRequest } from "bereach/models/operations";

let value: WithdrawInvitationRequest = {
  invitationId: "<id>",
};
```

## Fields

| Field                                                                                                                | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `invitationId`                                                                                                       | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | The invitation to withdraw: invitationId or invitationUrn from the sent invitations list                             |
| `profileUrn`                                                                                                         | *string*                                                                                                             | :heavy_minus_sign:                                                                                                   | toMember.profileUrn of the same entry. With publicIdentifier, firstName and lastName it saves reading the list again |
| `publicIdentifier`                                                                                                   | *string*                                                                                                             | :heavy_minus_sign:                                                                                                   | toMember.publicIdentifier of the same entry                                                                          |
| `firstName`                                                                                                          | *string*                                                                                                             | :heavy_minus_sign:                                                                                                   | targetFirstName of the same entry                                                                                    |
| `lastName`                                                                                                           | *string*                                                                                                             | :heavy_minus_sign:                                                                                                   | targetLastName of the same entry                                                                                     |