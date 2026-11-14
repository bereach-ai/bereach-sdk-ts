# Contacts

## Overview

Endpoints for managing contacts and lifecycle stages without requiring a campaign

### Available Operations

* [upsert](#upsert) - Create or upsert contacts (no campaign required)
* [search](#search) - Search and filter contacts
* [get](#get) - Get a single contact with campaigns
* [update](#update) - Update a contact
* [listActivities](#listactivities) - List activities for a contact
* [discard](#discard) - Discard or restore people, in bulk
* [stats](#stats) - Get contact funnel statistics
* [listCampaigns](#listcampaigns) - List campaigns
* [listByCampaign](#listbycampaign) - List contacts in a campaign
* [addToCampaign](#addtocampaign) - Add contacts to a campaign
* [getByUrl](#getbyurl) - Look up contact by LinkedIn URL
* [addSignals](#addsignals) - Add signals to a list
* [checkFit](#checkfit) - Check fit on a list
* [brief](#brief) - Brief one person
* [findEmails](#findemails) - Find work emails
* [findPhones](#findphones) - Find phone numbers

## upsert

Save people without creating a campaign first. Upserts by profile URL. Returns the saved rows.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="contactsUpsert" method="post" path="/contacts" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.upsert({
    contacts: [
      {
        linkedinUrl: "https://bleak-pulse.name/",
        name: "<value>",
      },
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
import { contactsUpsert } from "bereach/funcs/contacts-upsert.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsUpsert(bereach, {
    contacts: [
      {
        linkedinUrl: "https://bleak-pulse.name/",
        name: "<value>",
      },
    ],
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsUpsert failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="contactsUpsert" method="post" path="/contacts" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.upsert({
    contacts: [
      {
        linkedinUrl: "https://bleak-pulse.name/",
        name: "<value>",
      },
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
import { contactsUpsert } from "bereach/funcs/contacts-upsert.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsUpsert(bereach, {
    contacts: [
      {
        linkedinUrl: "https://bleak-pulse.name/",
        name: "<value>",
      },
    ],
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsUpsert failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ContactsUpsertRequest](../../models/operations/contacts-upsert-request.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ContactsUpsertResponse](../../models/operations/contacts-upsert-response.md)\>**

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

## search

Search saved people: name, profile URL, removed or still in the list, outreach status, tags, and list membership. Supports pagination and sorting.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="contactsSearch" method="get" path="/contacts/search" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.search({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsSearch } from "bereach/funcs/contacts-search.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsSearch(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsSearch failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ContactsSearchRequest](../../models/operations/contacts-search-request.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ContactsSearchResponse](../../models/operations/contacts-search-response.md)\>**

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

## get

Get one saved person: profile snapshot, outreach status and the lists they are in, with their stage in each. The activity log is contacts_get_activities.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="contactsGetFull" method="get" path="/contacts/{id}" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.get({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsGet } from "bereach/funcs/contacts-get.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsGet(bereach, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ContactsGetFullRequest](../../models/operations/contacts-get-full-request.md)                                                                                      | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ContactsGetFullResponse](../../models/operations/contacts-get-full-response.md)\>**

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

## update

Update notes, outreach status, tags or profile data for a person, or remove them from a list and bring them back. lifecycleStage is per-list: pass campaignId to scope the write to one list, or the request is rejected.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="contactsUpdate" method="patch" path="/contacts/{id}" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.update({
    id: "<id>",
    body: {},
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsUpdate } from "bereach/funcs/contacts-update.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsUpdate(bereach, {
    id: "<id>",
    body: {},
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsUpdate failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="contactsUpdate" method="patch" path="/contacts/{id}" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.update({
    id: "<id>",
    body: {},
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsUpdate } from "bereach/funcs/contacts-update.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsUpdate(bereach, {
    id: "<id>",
    body: {},
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsUpdate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ContactsUpdateRequest](../../models/operations/contacts-update-request.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ContactsUpdateResponse](../../models/operations/contacts-update-response.md)\>**

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

## listActivities

Get paginated activity log for a SPECIFIC contact. Requires contact id (path param): cannot list activities for all contacts. Call contacts_search first to get the contact id, then call this with that id.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="contactsGetActivities" method="get" path="/contacts/{id}/activities" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.listActivities({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsListActivities } from "bereach/funcs/contacts-list-activities.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsListActivities(bereach, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsListActivities failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ContactsGetActivitiesRequest](../../models/operations/contacts-get-activities-request.md)                                                                          | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ContactsGetActivitiesResponse](../../models/operations/contacts-get-activities-response.md)\>**

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

## discard

Remove people from the list in one call with update.lifecycleStage "rejected", or bring them back with "contact"; the write lands on this conversation's own list, so never name one. Asked to remove people by a RULE rather than by name, call filter_contacts first and write only the ids it returned: that way you are removing real rows rather than a guess, and you can say exactly who went and why, which you must. Never invent an id.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="discardContacts" method="patch" path="/contacts/bulk" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.discard({
    body: {
      contactIds: [
        "<value 1>",
        "<value 2>",
      ],
      update: {},
    },
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsDiscard } from "bereach/funcs/contacts-discard.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsDiscard(bereach, {
    body: {
      contactIds: [
        "<value 1>",
        "<value 2>",
      ],
      update: {},
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsDiscard failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="discardContacts" method="patch" path="/contacts/bulk" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.discard({
    body: {
      contactIds: [
        "<value 1>",
        "<value 2>",
      ],
      update: {},
    },
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsDiscard } from "bereach/funcs/contacts-discard.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsDiscard(bereach, {
    body: {
      contactIds: [
        "<value 1>",
        "<value 2>",
      ],
      update: {},
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsDiscard failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DiscardContactsRequest](../../models/operations/discard-contacts-request.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.DiscardContactsResponse](../../models/operations/discard-contacts-response.md)\>**

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

## stats

Counts for the list: people in it, people removed, source, and daily trends.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="contactsStats" method="get" path="/contacts/stats" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.stats();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsStats } from "bereach/funcs/contacts-stats.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsStats(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsStats failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ContactsStatsRequest](../../models/operations/contacts-stats-request.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ContactsStatsResponse](../../models/operations/contacts-stats-response.md)\>**

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

## listCampaigns

List campaigns with optional filters and stage counts.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="contactsListCampaigns" method="get" path="/contacts/campaigns" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.listCampaigns({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsListCampaigns } from "bereach/funcs/contacts-list-campaigns.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsListCampaigns(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsListCampaigns failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ContactsListCampaignsRequest](../../models/operations/contacts-list-campaigns-request.md)                                                                          | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ContactsListCampaignsResponse](../../models/operations/contacts-list-campaigns-response.md)\>**

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

## listByCampaign

List contacts in a campaign with optional filters.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="contactsList" method="get" path="/contacts/campaigns/{campaignId}/contacts" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.listByCampaign({
    campaignId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsListByCampaign } from "bereach/funcs/contacts-list-by-campaign.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsListByCampaign(bereach, {
    campaignId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsListByCampaign failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ContactsListRequest](../../models/operations/contacts-list-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ContactsListResponse](../../models/operations/contacts-list-response.md)\>**

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

## addToCampaign

Add contacts to a campaign (up to 500). Deduplicates by LinkedIn URL.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="contactsAdd" method="post" path="/contacts/campaigns/{campaignId}/contacts" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.addToCampaign({
    campaignId: "<id>",
    body: {
      contacts: [],
    },
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsAddToCampaign } from "bereach/funcs/contacts-add-to-campaign.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsAddToCampaign(bereach, {
    campaignId: "<id>",
    body: {
      contacts: [],
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsAddToCampaign failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="contactsAdd" method="post" path="/contacts/campaigns/{campaignId}/contacts" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.addToCampaign({
    campaignId: "<id>",
    body: {
      contacts: [],
    },
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsAddToCampaign } from "bereach/funcs/contacts-add-to-campaign.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsAddToCampaign(bereach, {
    campaignId: "<id>",
    body: {
      contacts: [],
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsAddToCampaign failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ContactsAddRequest](../../models/operations/contacts-add-request.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ContactsAddResponse](../../models/operations/contacts-add-response.md)\>**

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

## getByUrl

Find a contact by LinkedIn URL. Returns the person with the lists they are in.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="contactsGetByUrl" method="get" path="/contacts/by-url" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.getByUrl({
    linkedinUrl: "https://tough-apricot.org",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsGetByUrl } from "bereach/funcs/contacts-get-by-url.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsGetByUrl(bereach, {
    linkedinUrl: "https://tough-apricot.org",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsGetByUrl failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ContactsGetByUrlRequest](../../models/operations/contacts-get-by-url-request.md)                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ContactsGetByUrlResponse](../../models/operations/contacts-get-by-url-response.md)\>**

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

## addSignals

Starts, in the background, a run that gives each person on a list a dated reason to write to them now: a new role, their own recent posts, dated news about their company. Answers at once with the most the run costs; call again with start false for its progress.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="contactsAddSignals" method="post" path="/contacts/signals" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.addSignals({
    campaignId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsAddSignals } from "bereach/funcs/contacts-add-signals.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsAddSignals(bereach, {
    campaignId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsAddSignals failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="contactsAddSignals" method="post" path="/contacts/signals" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.addSignals({
    campaignId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsAddSignals } from "bereach/funcs/contacts-add-signals.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsAddSignals(bereach, {
    campaignId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsAddSignals failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ContactsAddSignalsRequest](../../models/operations/contacts-add-signals-request.md)                                                                                | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ContactsAddSignalsResponse](../../models/operations/contacts-add-signals-response.md)\>**

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

## checkFit

Scores each person on a list 0 to 100 against an ideal customer and its personas, with the persona each reads as and one line of why, and saves the setup on the list. Informative only: it hides and blocks nobody. Cost: a little per person scored, for the model reading them, at most the cost the reply gives; nothing when nobody is checked. Prices are quoted on Pro; pay as you go costs 30% more. spent is what the call cost at the user's own rate, in money: tell the user that amount as it is, never creditsUsed.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="contactsCheckFit" method="post" path="/contacts/fit-check" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.checkFit({
    campaignId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsCheckFit } from "bereach/funcs/contacts-check-fit.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsCheckFit(bereach, {
    campaignId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsCheckFit failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="contactsCheckFit" method="post" path="/contacts/fit-check" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.checkFit({
    campaignId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsCheckFit } from "bereach/funcs/contacts-check-fit.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsCheckFit(bereach, {
    campaignId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsCheckFit failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ContactsCheckFitRequest](../../models/operations/contacts-check-fit-request.md)                                                                                    | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ContactsCheckFitResponse](../../models/operations/contacts-check-fit-response.md)\>**

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

## brief

Everything worth knowing about one person before writing to them, in one answer: who they are and where they stand with the user, their recent posts, reactions and comments, their current company, dated reasons to write now, and the conversation with them (the latest messages whole, older ones summarized by day, week and month). A part that could not be read comes back empty with its reason; the conversation needs a connected account. Each part says when what it shows was read (readAt): live, unless an earlier read is younger than maxAgeDays. A reaction's post text, a comment and a recommendation are cut at 500 characters. A long conversation read for the first time takes longer. Cost: at most 0,05 € for a person read whole, plus a little for summarizing older messages, once per period; the conversation itself is free, and a part reused or not read costs nothing. Prices are quoted on Pro; pay as you go costs 30% more. spent is what the call cost at the user's own rate, in money: tell the user that amount as it is, never creditsUsed.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="contactsBrief" method="post" path="/contacts/brief" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.brief({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsBrief } from "bereach/funcs/contacts-brief.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsBrief(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsBrief failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="contactsBrief" method="post" path="/contacts/brief" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.brief({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsBrief } from "bereach/funcs/contacts-brief.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsBrief(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsBrief failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ContactsBriefRequest](../../models/operations/contacts-brief-request.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ContactsBriefResponse](../../models/operations/contacts-brief-response.md)\>**

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

## findEmails

Find the work email of up to 25 people, saved people by contact id or anyone by profile address, and keep each email found on the saved contact. Cost: 0,005 € an email found, from the same balance as every other read. A call that finds no email at all costs one email. Available through the API and the Claude connector.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="findEmails" method="post" path="/emails/find" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.findEmails({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsFindEmails } from "bereach/funcs/contacts-find-emails.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsFindEmails(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsFindEmails failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="findEmails" method="post" path="/emails/find" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.findEmails({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsFindEmails } from "bereach/funcs/contacts-find-emails.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsFindEmails(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsFindEmails failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.FindEmailsRequest](../../models/operations/find-emails-request.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.FindEmailsResponse](../../models/operations/find-emails-response.md)\>**

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

## findPhones

Find the phone number of up to 25 people, saved people by contact id or anyone by profile address. Cost: 0,25 € a phone number found, mobile or landline, from the same balance as every other read. A call that finds no number at all costs one number. Available through the API and the Claude connector.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="findPhones" method="post" path="/phones/find" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.findPhones({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsFindPhones } from "bereach/funcs/contacts-find-phones.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsFindPhones(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsFindPhones failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="findPhones" method="post" path="/phones/find" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.findPhones({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { contactsFindPhones } from "bereach/funcs/contacts-find-phones.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsFindPhones(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsFindPhones failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.FindPhonesRequest](../../models/operations/find-phones-request.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.FindPhonesResponse](../../models/operations/find-phones-response.md)\>**

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