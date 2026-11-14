# FindEmailsStopped

The five-hour usage limit, or a trial's cost cap, stopped the lookups part way with too little money added by card left to go on from: the people marked unavailable cost nothing. resetsAt is when the five-hour limit resets. Money added by card at topUpUrl is not held by either limit.

## Example Usage

```typescript
import { FindEmailsStopped } from "bereach/models/operations";

let value: FindEmailsStopped = {
  reason: "<value>",
  topUpUrl: "https://jealous-pulse.biz/",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `reason`           | *string*           | :heavy_check_mark: | N/A                |
| `resetsAt`         | *string*           | :heavy_minus_sign: | N/A                |
| `topUpUrl`         | *string*           | :heavy_check_mark: | N/A                |