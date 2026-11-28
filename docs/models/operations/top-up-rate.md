# TopUpRate

The rate topUp was bought at; its money value is topUp at this rate, never at the workspace's current rate

## Example Usage

```typescript
import { TopUpRate } from "bereach/models/operations";

let value: TopUpRate = "payg";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"pro" | "payg" | Unrecognized<string>
```