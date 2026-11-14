# Profile

## Overview

Endpoints for the authenticated user's own LinkedIn profile

### Available Operations

* [get](#get) - Get authenticated user's LinkedIn profile
* [listAccounts](#listaccounts) - List all LinkedIn accounts for the authenticated user
* [updateAccount](#updateaccount) - Update a LinkedIn account (label, default)
* [getLimits](#getlimits) - Get current LinkedIn quota status
* [getConnectionStatus](#getconnectionstatus) - Get the state of outgoing connection requests
* [getCredits](#getcredits) - Get what the workspace can still spend
* [switchAccount](#switchaccount) - Switch active LinkedIn account
* [listConnections](#listconnections) - List LinkedIn connections
* [listRecommendedPeople](#listrecommendedpeople) - List the people suggested to you
* [getMyPosts](#getmyposts) - Get the authenticated user's own posts
* [getSettings](#getsettings) - Get account settings
* [patchSettings](#patchsettings) - Update account settings

## get

Returns the authenticated user's LinkedIn profile as it is currently stored: identity, headline, profile URL, connection count, location, and verification status. Reads what is stored only and costs no credits. Enriched fields (about text, positions, education, recent posts, recent comments and reactions) appear only when an earlier call has already written them, so treat every one of them as optional and never assume the record is complete.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getProfile" method="get" path="/me/linkedin" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.get();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileGet } from "bereach/funcs/profile-get.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileGet(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetProfileResponse](../../models/operations/get-profile-response.md)\>**

### Errors

| Error Type                                | Status Code                               | Content Type                              |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| errors.BadRequestError                    | 400                                       | application/json                          |
| errors.UnauthorizedError                  | 401                                       | application/json                          |
| errors.ForbiddenError                     | 403                                       | application/json                          |
| errors.NotFoundError                      | 404                                       | application/json                          |
| errors.ConflictError                      | 409                                       | application/json                          |
| errors.GoneError                          | 410                                       | application/json                          |
| errors.UnprocessableEntityError           | 422                                       | application/json                          |
| errors.TooManyRequestsError               | 429                                       | application/json                          |
| errors.CollectEngagersInternalServerError | 500                                       | application/json                          |
| errors.BadGatewayError                    | 502                                       | application/json                          |
| errors.ServiceUnavailableError            | 503                                       | application/json                          |
| errors.BereachDefaultError                | 4XX, 5XX                                  | \*/\*                                     |

## listAccounts

Returns all LinkedIn accounts connected by the user. Each account has credentials and profile info. The `isCurrent` flag indicates which account the current API token is bound to.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listAccounts" method="get" path="/me/linkedin/accounts" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.listAccounts();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileListAccounts } from "bereach/funcs/profile-list-accounts.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileListAccounts(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileListAccounts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListAccountsResponse](../../models/operations/list-accounts-response.md)\>**

### Errors

| Error Type                                   | Status Code                                  | Content Type                                 |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| errors.ResponseBodyBadRequestError1          | 400                                          | application/json                             |
| errors.ResponseBodyBadRequestError2          | 400                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError1        | 401                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError2        | 401                                          | application/json                             |
| errors.ResponseBodyForbiddenError1           | 403                                          | application/json                             |
| errors.ResponseBodyForbiddenError2           | 403                                          | application/json                             |
| errors.ResponseBodyNotFoundError1            | 404                                          | application/json                             |
| errors.ResponseBodyNotFoundError2            | 404                                          | application/json                             |
| errors.ResponseBodyConflictError1            | 409                                          | application/json                             |
| errors.ResponseBodyConflictError2            | 409                                          | application/json                             |
| errors.ResponseBodyGoneError1                | 410                                          | application/json                             |
| errors.ResponseBodyGoneError2                | 410                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError1 | 422                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError2 | 422                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError1     | 429                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError2     | 429                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError1 | 500                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError2 | 500                                          | application/json                             |
| errors.ResponseBodyBadGatewayError1          | 502                                          | application/json                             |
| errors.ResponseBodyBadGatewayError2          | 502                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError1  | 503                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError2  | 503                                          | application/json                             |
| errors.BereachDefaultError                   | 4XX, 5XX                                     | \*/\*                                        |

## updateAccount

Update account metadata. Setting `isDefault: true` clears the default flag from all other accounts.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="updateAccount" method="patch" path="/me/linkedin/accounts" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.updateAccount({
    accountId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileUpdateAccount } from "bereach/funcs/profile-update-account.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileUpdateAccount(bereach, {
    accountId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileUpdateAccount failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="updateAccount" method="patch" path="/me/linkedin/accounts" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.updateAccount({
    accountId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileUpdateAccount } from "bereach/funcs/profile-update-account.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileUpdateAccount(bereach, {
    accountId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileUpdateAccount failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdateAccountRequest](../../models/operations/update-account-request.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.UpdateAccountResponse](../../models/operations/update-account-response.md)\>**

### Errors

| Error Type                                | Status Code                               | Content Type                              |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| errors.BadRequestError                    | 400                                       | application/json                          |
| errors.UnauthorizedError                  | 401                                       | application/json                          |
| errors.ForbiddenError                     | 403                                       | application/json                          |
| errors.NotFoundError                      | 404                                       | application/json                          |
| errors.ConflictError                      | 409                                       | application/json                          |
| errors.GoneError                          | 410                                       | application/json                          |
| errors.UnprocessableEntityError           | 422                                       | application/json                          |
| errors.TooManyRequestsError               | 429                                       | application/json                          |
| errors.CollectEngagersInternalServerError | 500                                       | application/json                          |
| errors.BadGatewayError                    | 502                                       | application/json                          |
| errors.ServiceUnavailableError            | 503                                       | application/json                          |
| errors.BereachDefaultError                | 4XX, 5XX                                  | \*/\*                                     |

## getLimits

Returns the current quota status for all LinkedIn action types. Includes current usage, effective quotas (with workspace multiplier applied), remaining capacity, minimum delay between actions in seconds, and next reset times.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getLimits" method="get" path="/me/limits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.getLimits();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileGetLimits } from "bereach/funcs/profile-get-limits.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileGetLimits(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileGetLimits failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetLimitsResponse](../../models/operations/get-limits-response.md)\>**

### Errors

| Error Type                                | Status Code                               | Content Type                              |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| errors.BadRequestError                    | 400                                       | application/json                          |
| errors.UnauthorizedError                  | 401                                       | application/json                          |
| errors.ForbiddenError                     | 403                                       | application/json                          |
| errors.NotFoundError                      | 404                                       | application/json                          |
| errors.ConflictError                      | 409                                       | application/json                          |
| errors.GoneError                          | 410                                       | application/json                          |
| errors.UnprocessableEntityError           | 422                                       | application/json                          |
| errors.TooManyRequestsError               | 429                                       | application/json                          |
| errors.CollectEngagersInternalServerError | 500                                       | application/json                          |
| errors.BadGatewayError                    | 502                                       | application/json                          |
| errors.ServiceUnavailableError            | 503                                       | application/json                          |
| errors.BereachDefaultError                | 4XX, 5XX                                  | \*/\*                                     |

## getConnectionStatus

Read-only, per connected account: whether invitations are going out, who is next, how many are waiting, and when nothing is going out, what is stopping it.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getConnectionStatus" method="get" path="/me/connection-status" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.getConnectionStatus();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileGetConnectionStatus } from "bereach/funcs/profile-get-connection-status.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileGetConnectionStatus(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileGetConnectionStatus failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetConnectionStatusResponse](../../models/operations/get-connection-status-response.md)\>**

### Errors

| Error Type                                | Status Code                               | Content Type                              |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| errors.BadRequestError                    | 400                                       | application/json                          |
| errors.UnauthorizedError                  | 401                                       | application/json                          |
| errors.ForbiddenError                     | 403                                       | application/json                          |
| errors.NotFoundError                      | 404                                       | application/json                          |
| errors.ConflictError                      | 409                                       | application/json                          |
| errors.GoneError                          | 410                                       | application/json                          |
| errors.UnprocessableEntityError           | 422                                       | application/json                          |
| errors.TooManyRequestsError               | 429                                       | application/json                          |
| errors.CollectEngagersInternalServerError | 500                                       | application/json                          |
| errors.BadGatewayError                    | 502                                       | application/json                          |
| errors.ServiceUnavailableError            | 503                                       | application/json                          |
| errors.BereachDefaultError                | 4XX, 5XX                                  | \*/\*                                     |

## getCredits

Returns what the workspace can still spend, in credits for code: the allowance used and its size for the current pool period (a calendar month on a plan or trial; on the free tier a one-time gift that never renews), the money added under pay as you go (topUp, never expiring, and the rate it was bought at), and remaining, which is the allowance left plus topUp. When isUnlimited is true, limit and remaining are null: skip credit budgeting. limits says the two buckets apart: the included use (allowance), held by the five-hour usage limit and on a trial its cap (each one's share, when the window resets, heldBy), and the money added by card (topUp), which no limit holds; while a limit holds the allowance, paid reads are paid from topUp alone.

### Example Usage: free

<!-- UsageSnippet language="typescript" operationID="getCredits" method="get" path="/me/credits" example="free" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.getCredits();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileGetCredits } from "bereach/funcs/profile-get-credits.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileGetCredits(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileGetCredits failed:", res.error);
  }
}

run();
```
### Example Usage: topUp

<!-- UsageSnippet language="typescript" operationID="getCredits" method="get" path="/me/credits" example="topUp" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.getCredits();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileGetCredits } from "bereach/funcs/profile-get-credits.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileGetCredits(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileGetCredits failed:", res.error);
  }
}

run();
```
### Example Usage: unlimited

<!-- UsageSnippet language="typescript" operationID="getCredits" method="get" path="/me/credits" example="unlimited" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.getCredits();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileGetCredits } from "bereach/funcs/profile-get-credits.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileGetCredits(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileGetCredits failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetCreditsResponse](../../models/operations/get-credits-response.md)\>**

### Errors

| Error Type                                | Status Code                               | Content Type                              |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| errors.BadRequestError                    | 400                                       | application/json                          |
| errors.UnauthorizedError                  | 401                                       | application/json                          |
| errors.ForbiddenError                     | 403                                       | application/json                          |
| errors.NotFoundError                      | 404                                       | application/json                          |
| errors.ConflictError                      | 409                                       | application/json                          |
| errors.GoneError                          | 410                                       | application/json                          |
| errors.UnprocessableEntityError           | 422                                       | application/json                          |
| errors.TooManyRequestsError               | 429                                       | application/json                          |
| errors.CollectEngagersInternalServerError | 500                                       | application/json                          |
| errors.BadGatewayError                    | 502                                       | application/json                          |
| errors.ServiceUnavailableError            | 503                                       | application/json                          |
| errors.BereachDefaultError                | 4XX, 5XX                                  | \*/\*                                     |

## switchAccount

Switch the active LinkedIn account. Connection requests and messages then go from the selected account.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="switchAccount" method="post" path="/me/switch-account" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.switchAccount({
    credentialsId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileSwitchAccount } from "bereach/funcs/profile-switch-account.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileSwitchAccount(bereach, {
    credentialsId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileSwitchAccount failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="switchAccount" method="post" path="/me/switch-account" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.switchAccount({
    credentialsId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileSwitchAccount } from "bereach/funcs/profile-switch-account.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileSwitchAccount(bereach, {
    credentialsId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileSwitchAccount failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SwitchAccountRequest](../../models/operations/switch-account-request.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SwitchAccountResponse](../../models/operations/switch-account-response.md)\>**

### Errors

| Error Type                                | Status Code                               | Content Type                              |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| errors.BadRequestError                    | 400                                       | application/json                          |
| errors.UnauthorizedError                  | 401                                       | application/json                          |
| errors.ForbiddenError                     | 403                                       | application/json                          |
| errors.NotFoundError                      | 404                                       | application/json                          |
| errors.ConflictError                      | 409                                       | application/json                          |
| errors.GoneError                          | 410                                       | application/json                          |
| errors.UnprocessableEntityError           | 422                                       | application/json                          |
| errors.TooManyRequestsError               | 429                                       | application/json                          |
| errors.CollectEngagersInternalServerError | 500                                       | application/json                          |
| errors.BadGatewayError                    | 502                                       | application/json                          |
| errors.ServiceUnavailableError            | 503                                       | application/json                          |
| errors.BereachDefaultError                | 4XX, 5XX                                  | \*/\*                                     |

## listConnections

List the people you are ALREADY connected to, first degree, newest first, with name, headline, profile URL and the date you connected, AND save each page into the contact list. This is your existing network, so use it to work people who already know you; for people you are not connected to yet ask for recommended people instead, and for where your outgoing invitations stand ask for connection status. Pages with `nextStart`. `saved` reports what that write actually stored.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getConnections" method="get" path="/me/linkedin/connections" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.listConnections({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileListConnections } from "bereach/funcs/profile-list-connections.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileListConnections(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileListConnections failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetConnectionsRequest](../../models/operations/get-connections-request.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetConnectionsResponse](../../models/operations/get-connections-response.md)\>**

### Errors

| Error Type                                | Status Code                               | Content Type                              |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| errors.BadRequestError                    | 400                                       | application/json                          |
| errors.UnauthorizedError                  | 401                                       | application/json                          |
| errors.ForbiddenError                     | 403                                       | application/json                          |
| errors.NotFoundError                      | 404                                       | application/json                          |
| errors.ConflictError                      | 409                                       | application/json                          |
| errors.GoneError                          | 410                                       | application/json                          |
| errors.UnprocessableEntityError           | 422                                       | application/json                          |
| errors.TooManyRequestsError               | 429                                       | application/json                          |
| errors.CollectEngagersInternalServerError | 500                                       | application/json                          |
| errors.BadGatewayError                    | 502                                       | application/json                          |
| errors.ServiceUnavailableError            | 503                                       | application/json                          |
| errors.BereachDefaultError                | 4XX, 5XX                                  | \*/\*                                     |

## listRecommendedPeople

List the people suggested to your account on My Network, with name, headline, profile URL and the reason given for each, AND save them into the contact list. These are people you are NOT connected to, so it answers who is worth meeting rather than who you already know; use the connections list for people already in your network. Returns one set per call and cannot continue from where it stopped, so ask once for the number wanted. `saved` reports what the write actually stored.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getRecommendedPeople" method="get" path="/me/linkedin/recommended" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.listRecommendedPeople();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileListRecommendedPeople } from "bereach/funcs/profile-list-recommended-people.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileListRecommendedPeople(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileListRecommendedPeople failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetRecommendedPeopleRequest](../../models/operations/get-recommended-people-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetRecommendedPeopleResponse](../../models/operations/get-recommended-people-response.md)\>**

### Errors

| Error Type                                | Status Code                               | Content Type                              |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| errors.BadRequestError                    | 400                                       | application/json                          |
| errors.UnauthorizedError                  | 401                                       | application/json                          |
| errors.ForbiddenError                     | 403                                       | application/json                          |
| errors.NotFoundError                      | 404                                       | application/json                          |
| errors.ConflictError                      | 409                                       | application/json                          |
| errors.GoneError                          | 410                                       | application/json                          |
| errors.UnprocessableEntityError           | 422                                       | application/json                          |
| errors.TooManyRequestsError               | 429                                       | application/json                          |
| errors.CollectEngagersInternalServerError | 500                                       | application/json                          |
| errors.BadGatewayError                    | 502                                       | application/json                          |
| errors.ServiceUnavailableError            | 503                                       | application/json                          |
| errors.BereachDefaultError                | 4XX, 5XX                                  | \*/\*                                     |

## getMyPosts

List posts authored by the authenticated user, newest first, with pagination, each with its media when it has some (pictures, a video, or a carousel's PDF and pages). Up to date, newest first. Cost: at most 0,005 € a page, posts or none; nothing when the page could not be read.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getOwnPosts" method="post" path="/me/linkedin/posts" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.getMyPosts();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileGetMyPosts } from "bereach/funcs/profile-get-my-posts.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileGetMyPosts(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileGetMyPosts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetOwnPostsRequest](../../models/operations/get-own-posts-request.md)                                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetOwnPostsResponse](../../models/operations/get-own-posts-response.md)\>**

### Errors

| Error Type                                | Status Code                               | Content Type                              |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| errors.BadRequestError                    | 400                                       | application/json                          |
| errors.UnauthorizedError                  | 401                                       | application/json                          |
| errors.ForbiddenError                     | 403                                       | application/json                          |
| errors.NotFoundError                      | 404                                       | application/json                          |
| errors.ConflictError                      | 409                                       | application/json                          |
| errors.GoneError                          | 410                                       | application/json                          |
| errors.UnprocessableEntityError           | 422                                       | application/json                          |
| errors.TooManyRequestsError               | 429                                       | application/json                          |
| errors.CollectEngagersInternalServerError | 500                                       | application/json                          |
| errors.BadGatewayError                    | 502                                       | application/json                          |
| errors.ServiceUnavailableError            | 503                                       | application/json                          |
| errors.BereachDefaultError                | 4XX, 5XX                                  | \*/\*                                     |

## getSettings

Returns user profile, location, connection settings, subscription, LinkedIn accounts, and pending invites.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getSettings" method="get" path="/me/settings" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.getSettings();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profileGetSettings } from "bereach/funcs/profile-get-settings.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profileGetSettings(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profileGetSettings failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetSettingsResponse](../../models/operations/get-settings-response.md)\>**

### Errors

| Error Type                                   | Status Code                                  | Content Type                                 |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| errors.ResponseBodyBadRequestError1          | 400                                          | application/json                             |
| errors.ResponseBodyBadRequestError2          | 400                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError1        | 401                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError2        | 401                                          | application/json                             |
| errors.ResponseBodyForbiddenError1           | 403                                          | application/json                             |
| errors.ResponseBodyForbiddenError2           | 403                                          | application/json                             |
| errors.ResponseBodyNotFoundError1            | 404                                          | application/json                             |
| errors.ResponseBodyNotFoundError2            | 404                                          | application/json                             |
| errors.ResponseBodyConflictError1            | 409                                          | application/json                             |
| errors.ResponseBodyConflictError2            | 409                                          | application/json                             |
| errors.ResponseBodyGoneError1                | 410                                          | application/json                             |
| errors.ResponseBodyGoneError2                | 410                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError1 | 422                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError2 | 422                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError1     | 429                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError2     | 429                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError1 | 500                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError2 | 500                                          | application/json                             |
| errors.ResponseBodyBadGatewayError1          | 502                                          | application/json                             |
| errors.ResponseBodyBadGatewayError2          | 502                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError1  | 503                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError2  | 503                                          | application/json                             |
| errors.BereachDefaultError                   | 4XX, 5XX                                     | \*/\*                                        |

## patchSettings

Update user country, city, or phone. A location change also updates the connection settings of the accounts.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="patchSettings" method="patch" path="/me/settings" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.patchSettings({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profilePatchSettings } from "bereach/funcs/profile-patch-settings.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profilePatchSettings(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profilePatchSettings failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="patchSettings" method="patch" path="/me/settings" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.profile.patchSettings({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { profilePatchSettings } from "bereach/funcs/profile-patch-settings.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await profilePatchSettings(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profilePatchSettings failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PatchSettingsRequest](../../models/operations/patch-settings-request.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PatchSettingsResponse](../../models/operations/patch-settings-response.md)\>**

### Errors

| Error Type                                   | Status Code                                  | Content Type                                 |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| errors.ResponseBodyBadRequestError1          | 400                                          | application/json                             |
| errors.ResponseBodyBadRequestError2          | 400                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError1        | 401                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError2        | 401                                          | application/json                             |
| errors.ResponseBodyForbiddenError1           | 403                                          | application/json                             |
| errors.ResponseBodyForbiddenError2           | 403                                          | application/json                             |
| errors.ResponseBodyNotFoundError1            | 404                                          | application/json                             |
| errors.ResponseBodyNotFoundError2            | 404                                          | application/json                             |
| errors.ResponseBodyConflictError1            | 409                                          | application/json                             |
| errors.ResponseBodyConflictError2            | 409                                          | application/json                             |
| errors.ResponseBodyGoneError1                | 410                                          | application/json                             |
| errors.ResponseBodyGoneError2                | 410                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError1 | 422                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError2 | 422                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError1     | 429                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError2     | 429                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError1 | 500                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError2 | 500                                          | application/json                             |
| errors.ResponseBodyBadGatewayError1          | 502                                          | application/json                             |
| errors.ResponseBodyBadGatewayError2          | 502                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError1  | 503                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError2  | 503                                          | application/json                             |
| errors.BereachDefaultError                   | 4XX, 5XX                                     | \*/\*                                        |