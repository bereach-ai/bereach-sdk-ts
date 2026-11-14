# Engagement

## Overview

People engaging with a post (likes, comments) and a profile's posts

### Available Operations

* [collectEngagers](#collectengagers) - Collect people on a post
* [collectPosts](#collectposts) - Collect posts of a profile
* [visitProfile](#visitprofile) - Read one person's public profile (kept for existing callers)
* [getFeed](#getfeed) - Get home feed

## collectEngagers

Everyone who reacted to or commented on up to 10 posts, replies included, saved as contacts and into the caller's list. Any public post works. One call reads one page of each list per post; untilCount reads page after page until that many people are saved or every list has ended, and more true continues where the last call stopped. With save skip they are read without being saved, to choose first. Each person comes with their name, headline, profile and photo, and their reaction or what they wrote, up to date, in 1 to 2 seconds a page of up to 100 people. Cost: 0,0005 € a person collected; a call that brings nobody costs one person; a post already read again within the hour costs nothing. Prices are quoted on Pro; pay as you go costs 30% more. spent is what the call cost at the user's own rate, in money: tell the user that amount as it is, never creditsUsed.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="collectEngagers" method="post" path="/collect/linkedin/engagers" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.engagement.collectEngagers({
    postUrls: [
      "<value 1>",
      "<value 2>",
    ],
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { engagementCollectEngagers } from "bereach/funcs/engagement-collect-engagers.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await engagementCollectEngagers(bereach, {
    postUrls: [
      "<value 1>",
      "<value 2>",
    ],
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("engagementCollectEngagers failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="collectEngagers" method="post" path="/collect/linkedin/engagers" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.engagement.collectEngagers({
    postUrls: [
      "<value 1>",
      "<value 2>",
    ],
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { engagementCollectEngagers } from "bereach/funcs/engagement-collect-engagers.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await engagementCollectEngagers(bereach, {
    postUrls: [
      "<value 1>",
      "<value 2>",
    ],
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("engagementCollectEngagers failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CollectEngagersRequest](../../models/operations/collect-engagers-request.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.CollectEngagersResponse](../../models/operations/collect-engagers-response.md)\>**

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

## collectPosts

Recent posts of a person or a company page, newest first, each with its text, date, reaction, comment and share counts, its author and its media when it has some (pictures, a video, or a carousel's PDF and pages). Set more true only if the user asked for another page or tapped Load more. For their posts on one subject, give topic. Full reads the recent posts a page at a time, newest first, up to date, in about 2 seconds a page; preview reads the latest few, with likes only, in about 3 seconds. Cost: 0,005 € a page of posts, on full or preview, posts or none; a topic is priced as a post search; nothing when the page could not be read. Prices are quoted on Pro; pay as you go costs 30% more. spent is what the call cost at the user's own rate, in money: tell the user that amount as it is, never creditsUsed.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="collectPosts" method="post" path="/collect/linkedin/posts" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.engagement.collectPosts({
    profileUrl: "https://all-fuel.org/",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { engagementCollectPosts } from "bereach/funcs/engagement-collect-posts.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await engagementCollectPosts(bereach, {
    profileUrl: "https://all-fuel.org/",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("engagementCollectPosts failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="collectPosts" method="post" path="/collect/linkedin/posts" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.engagement.collectPosts({
    profileUrl: "https://all-fuel.org/",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { engagementCollectPosts } from "bereach/funcs/engagement-collect-posts.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await engagementCollectPosts(bereach, {
    profileUrl: "https://all-fuel.org/",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("engagementCollectPosts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CollectPostsRequest](../../models/operations/collect-posts-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.CollectPostsResponse](../../models/operations/collect-posts-response.md)\>**

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

## visitProfile

Read one person. detail "preview" (default): a quick look; it can miss the current title and older posts. "full": every detail we have. Choose full for one person when the job title, how long they have held it, or the whole dated career matters. Preview gives the name, current employer, place, photo, follower count, the opening of the About and the latest posts, in about 3 seconds. Full gives the real headline, the current title with its start date, the dated career, schools, place and country, the About, languages and the connection and follower counts, usually live (readAt says when an older copy was used), in about 2 seconds a person. Cost: 0,005 € a person read, on preview or full, found or not; nothing for a person a search already returned or one that could not be read. Prices are quoted on Pro; pay as you go costs 30% more. spent is what the call cost at the user's own rate, in money: tell the user that amount as it is, never creditsUsed. New callers use publicProfile.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="visitProfile" method="post" path="/visit/linkedin/profile" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.engagement.visitProfile({
    profile: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { engagementVisitProfile } from "bereach/funcs/engagement-visit-profile.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await engagementVisitProfile(bereach, {
    profile: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("engagementVisitProfile failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="visitProfile" method="post" path="/visit/linkedin/profile" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.engagement.visitProfile({
    profile: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { engagementVisitProfile } from "bereach/funcs/engagement-visit-profile.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await engagementVisitProfile(bereach, {
    profile: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("engagementVisitProfile failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.VisitProfileRequest](../../models/operations/visit-profile-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.VisitProfileResponse](../../models/operations/visit-profile-response.md)\>**

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

## getFeed

Get posts from your home feed, most relevant (RELEVANCE) or newest first (REV_CHRON), each with its author, text and engagement counts.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getFeed" method="post" path="/feed/linkedin" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.engagement.getFeed({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { engagementGetFeed } from "bereach/funcs/engagement-get-feed.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await engagementGetFeed(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("engagementGetFeed failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetFeedRequest](../../models/operations/get-feed-request.md)                                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetFeedResponse](../../models/operations/get-feed-response.md)\>**

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