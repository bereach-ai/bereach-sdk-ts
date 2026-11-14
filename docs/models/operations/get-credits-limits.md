# GetCreditsLimits

The two buckets: the included use, held by the five-hour usage limit and a trial's cap, and the money added by card, which no limit holds

## Example Usage

```typescript
import { GetCreditsLimits } from "bereach/models/operations";

let value: GetCreditsLimits = {
  allowance: {
    window: {
      usedPercent: 3928.3,
      resetsAt: "<value>",
    },
    trialCap: {
      usedPercent: 7435.5,
    },
    heldBy: "window",
    left: true,
  },
  topUp: {
    left: true,
    limited: false,
  },
  topUpUrl: "https://self-reliant-reporter.biz",
  note: "<value>",
};
```

## Fields

| Field                                                                                                          | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `allowance`                                                                                                    | [operations.Allowance](../../models/operations/allowance.md)                                                   | :heavy_check_mark:                                                                                             | What the plan, the trial or the free tier includes: held by the five-hour usage limit and, on a trial, its cap |
| `topUp`                                                                                                        | [operations.TopUp](../../models/operations/top-up.md)                                                          | :heavy_check_mark:                                                                                             | The money added by card, a bucket of its own                                                                   |
| `topUpUrl`                                                                                                     | *string*                                                                                                       | :heavy_check_mark:                                                                                             | Where money is added by card                                                                                   |
| `note`                                                                                                         | *string*                                                                                                       | :heavy_check_mark:                                                                                             | Where the limits stand, in one or two sentences to say as written                                              |