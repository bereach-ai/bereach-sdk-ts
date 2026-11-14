# Search

## Overview

Find posts, people, companies and jobs, and turn a written label into the id a filter takes.

### Available Operations

* [posts](#posts) - Search posts
* [people](#people) - Search people
* [companies](#companies) - Search companies
* [jobs](#jobs) - Search job ads
* [searchParameters](#searchparameters) - Turn text into the ids LinkedIn filters take

## posts

# Search posts

Find posts matching your keywords and filters. This is the same search as **publicFindPosts**, at the same price, in this address's own request and response fields. Returns post text, engagement counts, author info and URLs. The post authors are saved to your contacts.

## Required parameters
- **keywords** (string, required): searched as written. Quoted phrases and OR alternatives are kept: `"growth hacking" OR "growth marketing"`.

## Filters
| Filter | Type | Description |
|--------|------|-------------|
| `datePosted` | `"past-24h"` \| `"past-week"` \| `"past-month"` | Only posts from this window |
| `authorJobTitle` | string[] | The author's job title, free text; several are searched as alternatives |
| `authorCompany` | string[] | Posts by people at this company, by name (one company) |
| `contentType` | `"images"` \| `"videos"` \| `"documents"` | Only posts carrying this media (not with `authorCompany`) |

`sortBy`, `authorIndustry` and `postedBy` are accepted and not applied: each is named in `ignoredFields`, with a NOT_SEARCHED warning saying why, as is any field this search does not read.

## Response fields (per item)
| Field | Type | Description |
|-------|------|-------------|
| `postUrl` | string | Direct URL to the post |
| `text` | string | Post text |
| `date` | number\|null | Publication timestamp (ms since epoch) |
| `likesCount` | number\|null | Total reactions |
| `commentsCount` | number\|null | Total comments |
| `sharesCount` | null | Not provided |
| `postUrn` / `postId` | string\|null | The activity URN and id, for collect_engagers |
| `author.name` / `author.profileUrl` / `author.headline` | string\|null | Who posted |
| `author.isCompany` | boolean | Whether the author is a company page |
| `isRepost` | null | Not provided |

## Pagination
- Default page size: 20, max 50
- `start` 0 is the first page; any `start` past 0 returns the next posts this same search had not yet returned to you (not an exact offset)
- `hasMore` says whether another page can come back; `paging.total` is always null

## Credits
Cost: 0,0025 € a post returned; a search that returns none costs one post.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="searchPosts" method="post" path="/search/linkedin/posts" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.posts({
    keywords: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchPosts } from "bereach/funcs/search-posts.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchPosts(bereach, {
    keywords: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchPosts failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="searchPosts" method="post" path="/search/linkedin/posts" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.posts({
    keywords: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchPosts } from "bereach/funcs/search-posts.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchPosts(bereach, {
    keywords: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchPosts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchPostsRequest](../../models/operations/search-posts-request.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchPostsResponse](../../models/operations/search-posts-response.md)\>**

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

## people

# Search people

Find professionals by name, title, company, location, industry, and more. Returns structured profile data including name, headline, current positions, connection degree, profile picture, **plus**: `nameMatch` (true when the result matched on the literal name), `badgeText` (Top Voice / Premium / Verified / Influencer), `ringStatus` (OPEN_TO_WORK / HIRING: open intent signals you can directly target), `summary` (additional snippet beyond headline), `actorInsights` (short context lines such as 'X mutual connections' or 'Follows {company}': use them directly in personalised openers).

## Parameters
- **keywords** (optional): Search terms matched against name, headline, company, skills, and bio
- You can search by filters alone (no keywords): e.g. find all 2nd-degree connections in Paris
- **A profile address as the keywords** (a profile link and nothing else): answered as that one person, read in full, charged as one person found; nobody, charged as one person, when the address names no profile; a later page is empty
- **One person asked** (`count` 1, keywords, no `firstName` or `lastName`, not a role at a company): the person found is kept only when a word of their name is in the keywords. Otherwise the answer is a success with nobody, charged as one person, `reason: "name_missing"` and a warning: add a first and last name

## Keyword syntax (Boolean operators)
Keywords support LinkedIn Boolean search syntax:
- **Exact phrase**: `"product manager"`: matches only that exact title
- **AND**: `engineer AND startup`, both terms required (spaces default to AND)
- **OR**: `CEO OR founder OR CTO`, any of the terms
- **NOT**: `manager NOT assistant`, exclude unwanted terms
- **Parentheses**: `(CEO OR CTO) AND SaaS`, group logic

Operators must be **UPPERCASE**. Precedence: Quotes > Parentheses > NOT > AND > OR.

## Available filters
Pass HUMAN LABELS for location / industry / currentCompany / pastCompany / school: the server resolves them to LinkedIn IDs via typeahead. Numeric IDs pass through unchanged if you already have them.

| Filter | Type | Description |
|--------|------|-------------|
| `connectionDegree` | `["F"\|"S"\|"O"]` | Connection level: F=1st, S=2nd, O=3rd+ |
| `firstName` | string | Exact first name match |
| `lastName` | string | Exact last name match |
| `title` | string | Current job title (supports `\|` OR syntax: `"CEO\|CTO"`) |
| `connectionOf` | string | Profile URN: find their connections |
| `followersOf` | string[] | Profile URNs: find a creator's followers |
| `openToVolunteering` | boolean | Only people open to volunteering |
| `serviceCategories` | string[] | Service-Marketplace category names |
| `profileLanguage` | string[] | ISO 639-1 codes: `["en","fr"]` |
| `location` | string[] | Geo labels (e.g. `["Paris","France"]`): resolved server-side |
| `industry` | string[] | Industry labels (e.g. `["Software Development"]`): resolved server-side |
| `currentCompany` | string[] | Company labels (e.g. `["Stripe","Datadog"]`): resolved server-side |
| `pastCompany` | string[] | Company labels: resolved server-side |
| `school` | string[] | School/university labels: resolved server-side |

## Response fields (per item)
| Field | Type | Description |
|-------|------|-------------|
| `name` | string | Full display name |
| `profileUrl` | string | LinkedIn profile URL |
| `headline` | string\|null | Professional headline |
| `location` | string\|null | Geographic location |
| `profilePicture` | string\|null | Profile photo URL |
| `networkDistance` | string\|null | `DISTANCE_1`, `DISTANCE_2`, `DISTANCE_3`, or `OUT_OF_NETWORK` |
| `currentPositions` | array | Current job positions with `company` and `role` |

## Pagination
- Default page size: 10, max 50
- Use `start` + `count` to paginate. Check `hasMore` for more pages.
- Paginate via `start` + `count`; check `hasMore` for more pages.

## Example workflows
1. **Prospect list building**: Search by title + location + industry → build a targeted outreach list
2. **Recruiting**: Search by title + company + school → find people who match
3. **Network mapping**: Search `connectionOf` + filters → explore someone's network

## Workflow: pass labels directly
```
POST /search/linkedin/people {
  keywords: 'product manager',
  location: ['San Francisco'],
  currentCompany: ['Google']
}
→ server resolves labels → matching people
```
Only call `/search/linkedin/parameters` when you need to EXPLORE available values ("what are the canonical industry buckets?"), never as a prerequisite to a search.

## Credits
Cost: 0,005 € a result returned; a search that returns none costs one result.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="searchPeople" method="post" path="/search/linkedin/people" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.people({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchPeople } from "bereach/funcs/search-people.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchPeople(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchPeople failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="searchPeople" method="post" path="/search/linkedin/people" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.people({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchPeople } from "bereach/funcs/search-people.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchPeople(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchPeople failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchPeopleRequest](../../models/operations/search-people-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchPeopleResponse](../../models/operations/search-people-response.md)\>**

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

## companies

# Search companies

Find companies by what they do or their name, place, industry and size. This is the same search as **publicFindCompanies**, at the same price, in this address's own request and response fields. Returns name, profileUrl, summary, industry, location, logoUrl, and besides them the website, headcount and founding year. `profileUrl` is null when the company's page is not known: pass the row's `name` to **publicCompany** to resolve it.

A company's name alone (`keywords` with no location, industry or size, and no quote or OR) is looked up rather than searched: the answer is that one company, read as **publicCompany** reads it, or no company with a NOT_FOUND warning when no company page carries the name. Add a location or an industry to search companies by the words instead.

## Filters (at least one of keywords, location or industry)
| Filter | Type | Description |
|--------|------|-------------|
| `keywords` | string | What the companies are or do, or a company's name |
| `location` | string[] | Places by name (e.g. `["Paris","France"]`) |
| `industry` | string[] | Industries by name (e.g. `["Software Development"]`) |
| `companySize` | string[] | Band codes A to I or a human range, searched as one span |

A numeric LinkedIn id for a place or an industry, and any field this search does not read, is accepted and not applied: each is named in `ignoredFields`, with a NOT_SEARCHED warning saying why.

## Response fields (per item)
| Field | Type | Description |
|-------|------|-------------|
| `name` | string | Company name |
| `profileUrl` | string\|null | LinkedIn company page, when known |
| `summary` | string\|null | What the company says it does |
| `industry` | string\|null | Industry |
| `location` | string\|null | City and country code |
| `followersCount` | number\|null | Followers, on a company looked up by its name; null otherwise |
| `logoUrl` | string\|null | Logo |
| `website` | string\|null | Homepage |
| `employees` | number\|null | Headcount |
| `foundedYear` | number\|null | Founding year |

## Pagination
- Default page size: 10, max 50
- `start` 0 is the first page; any `start` past 0 returns the next companies this same search had not yet returned to you (not an exact offset)
- `hasMore` says whether another page can come back; `paging.total` is always null

## Credits
Cost: 0,005 € a company returned; a search that returns none costs one company.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="searchCompanies" method="post" path="/search/linkedin/companies" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.companies({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchCompanies } from "bereach/funcs/search-companies.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchCompanies(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchCompanies failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="searchCompanies" method="post" path="/search/linkedin/companies" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.companies({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchCompanies } from "bereach/funcs/search-companies.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchCompanies(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchCompanies failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchCompaniesRequest](../../models/operations/search-companies-request.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchCompaniesResponse](../../models/operations/search-companies-response.md)\>**

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

## jobs

# Search job ads

Find job listings by keywords, location, job type, experience level, and workplace type. Returns lightweight job rows (title, company, companyUrl, companyLogo, location, workplaceType, postedAt, jobUrl, listingId).

## Parameters
- **keywords** (optional): Search terms matched against job title, company name, and description

## Keyword syntax (Boolean operators)
Keywords support LinkedIn Boolean search syntax:
- **Exact phrase**: `"frontend engineer"`: matches only that exact title
- **AND**: `React AND TypeScript`, both terms required (spaces default to AND)
- **OR**: `"frontend engineer" OR "front-end developer"`: either term
- **NOT**: `engineer NOT intern`, exclude unwanted terms
- **Parentheses**: `(React OR Vue) AND "senior engineer"`: group logic

Operators must be **UPPERCASE**. Precedence: Quotes > Parentheses > NOT > AND > OR.

## Available filters
Pass human-readable names for `location`, `company`, `industry`, `jobFunction`, `benefits`, `commitments`: they are resolved to LinkedIn IDs server-side. Do not hand-resolve.

| Filter | Type | Description |
|--------|------|-------------|
| `location` | string[] | City/region/country names |
| `company` | string[] | Hiring company names |
| `industry` | string[] | Company industry names |
| `jobFunction` | string[] | Job function names (Engineering, Sales, …) |
| `datePosted` | string | `"past-24h"` \| `"past-week"` \| `"past-month"` |
| `sortBy` | string | `"relevance"` \| `"date"` |
| `jobType` | string[] | Employment type codes (see below) |
| `experienceLevel` | string[] | Seniority codes (see below) |
| `workplaceType` | string[] | Work location codes (see below) |
| `benefits` | string[] | Advertised benefit names |
| `commitments` | string[] | Employer commitment names |
| `easyApply` | boolean | Only Easy Apply jobs |
| `under10Applicants` | boolean | Only jobs with <10 applicants |
| `inYourNetwork` | boolean | Only jobs where you have a connection |
| `hasVerifications` | boolean | Only verified job posters |
| `fairChanceEmployer` | boolean | Only Fair Chance employers |

### Job type codes
| Code | Type |
|------|------|
| `F` | Full-time |
| `P` | Part-time |
| `C` | Contract |
| `T` | Temporary |
| `I` | Internship |
| `V` | Volunteer |
| `O` | Other |

### Experience level codes
| Code | Level |
|------|-------|
| `1` | Internship |
| `2` | Entry level |
| `3` | Associate |
| `4` | Mid-Senior level |
| `5` | Director |
| `6` | Executive |

### Workplace type codes
| Code | Type |
|------|------|
| `1` | On-site |
| `2` | Remote |
| `3` | Hybrid |

## Response fields (per item)
| Field | Type | Description |
|-------|------|-------------|
| `title` | string | Job title |
| `company` | string\|null | Hiring company name |
| `companyUrl` | string\|null | Company LinkedIn page URL |
| `companyLogo` | string\|null | Company logo URL |
| `location` | string\|null | Job location |
| `workplaceType` | string\|null | On-site / Remote / Hybrid |
| `postedAt` | string\|null | Human-readable posting time (e.g. `"2 days ago"`) |
| `jobUrl` | string | Direct URL to the job listing |
| `listingId` | string | LinkedIn job listing ID |

## Pagination
- Default page size: 50, max 100
- Use `start` + `count` to paginate. Check `hasMore` for more pages.

## Example workflows
1. **Job monitoring**: Search by title + location → track new openings in your area
2. **Competitive hiring analysis**: Search by company keywords → see what roles competitors are hiring for
3. **Market demand research**: Search by skills → gauge demand for specific expertise

## Credits
Cost: 0,005 € a result returned; a search that returns none costs one result.

### Example Usage: credits

<!-- UsageSnippet language="typescript" operationID="searchJobs" method="post" path="/search/linkedin/jobs" example="credits" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.jobs({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchJobs } from "bereach/funcs/search-jobs.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchJobs(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchJobs failed:", res.error);
  }
}

run();
```
### Example Usage: pacing

<!-- UsageSnippet language="typescript" operationID="searchJobs" method="post" path="/search/linkedin/jobs" example="pacing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.jobs({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchJobs } from "bereach/funcs/search-jobs.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchJobs(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchJobs failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchJobsRequest](../../models/operations/search-jobs-request.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchJobsResponse](../../models/operations/search-jobs-response.md)\>**

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

## searchParameters

Resolve a written label (an industry, a company, a place, a school) into the identifier a search filter needs. Worth knowing why this exists: a filter given an id it does not recognise is accepted and ignored, so a search built on a guessed id quietly returns the unfiltered set and reads as a market with nobody in it. Leaving the keywords empty on a closed-value type lists every option, which is the way to answer what the available buckets are.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchParameters" method="get" path="/search/linkedin/parameters" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.searchParameters({
    type: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchSearchParameters } from "bereach/funcs/search-search-parameters.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchSearchParameters(bereach, {
    type: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchSearchParameters failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchParametersRequest](../../models/operations/search-parameters-request.md)                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchParametersResponse](../../models/operations/search-parameters-response.md)\>**

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