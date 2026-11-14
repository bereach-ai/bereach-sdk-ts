# Tasks

## Overview

Endpoints for reading the agent session snapshot

### Available Operations

* [eventsFeed](#eventsfeed) - Poll for events
* [agentSnapshot](#agentsnapshot) - Agent session snapshot

## eventsFeed

Returns recent alerts and activity: replies received, connections accepted, and warnings about a LinkedIn account that signed out or an AI error. Use the cursor to poll for newer ones. Events expire after 48 hours.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="eventsFeed" method="get" path="/events/feed" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.tasks.eventsFeed({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { tasksEventsFeed } from "bereach/funcs/tasks-events-feed.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await tasksEventsFeed(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("tasksEventsFeed failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.EventsFeedRequest](../../models/operations/events-feed-request.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.EventsFeedResponse](../../models/operations/events-feed-response.md)\>**

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

## agentSnapshot

Account snapshot: pipeline, every saved context, pending drafts, accounts and events in one call. Call it for any of those facts; to read one saved context use context_list by type= and scope=.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="contextGet" method="get" path="/agent/snapshot" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.tasks.agentSnapshot();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { tasksAgentSnapshot } from "bereach/funcs/tasks-agent-snapshot.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await tasksAgentSnapshot(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("tasksAgentSnapshot failed:", res.error);
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

**Promise\<[operations.ContextGetResponse](../../models/operations/context-get-response.md)\>**

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