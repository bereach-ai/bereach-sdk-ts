# PlanSearchesResponse

Questions to ask, a ready plan, or nothing to search


## Supported Types

### `operations.PlanSearchesResponseBody1`

```typescript
const value: operations.PlanSearchesResponseBody1 = {
  planId: "<id>",
  version: 449173,
  ready: false,
  assumptions: [
    {
      fact: "<value>",
      origin: "inferred",
      source: "<value>",
      use: "search",
      applied: true,
    },
  ],
  questions: [],
  segments: [],
  searches: [
    {
      id: "<id>",
      segment: "<value>",
      language: "<value>",
      where: "<value>",
      queries: [
        "<value 1>",
        "<value 2>",
        "<value 3>",
      ],
    },
  ],
  next: "<value>",
};
```

### `operations.PlanSearchesResponseBody2`

```typescript
const value: operations.PlanSearchesResponseBody2 = {
  planId: "<id>",
  version: 651469,
  ready: true,
  assumptions: [],
  questions: [
    {
      id: "<id>",
      question: "<value>",
      options: [],
    },
  ],
  segments: [
    {
      id: "<id>",
      name: "<value>",
      confidence: "low",
      kinds: [
        "<value 1>",
        "<value 2>",
        "<value 3>",
      ],
      places: [
        "<value 1>",
      ],
      groups: [
        {
          id: "<id>",
          name: "<value>",
        },
      ],
      evidence: [
        {
          source: "<value>",
          quote: "<value>",
        },
      ],
    },
  ],
  searches: [
    {
      id: "<id>",
      segment: "<value>",
      language: "<value>",
      where: "<value>",
      queries: [
        "<value 1>",
        "<value 2>",
      ],
    },
  ],
  peopleUpTo: 380902,
  costEstimateCredits: 96275,
  costLikelyCredits: 156052,
  next: "<value>",
};
```

### `operations.PlanSearchesResponseBody3`

```typescript
const value: operations.PlanSearchesResponseBody3 = {
  reason: "<value>",
  searches: [
    {
      id: "<id>",
      segment: "<value>",
      language: "<value>",
      where: "<value>",
      queries: [
        "<value 1>",
      ],
    },
  ],
  next: "<value>",
};
```

