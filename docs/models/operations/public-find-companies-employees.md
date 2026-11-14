# PublicFindCompaniesEmployees

Headcount range: only companies with between min and max employees. Only a size the person asked for in this conversation, kept while they continue that ask; never from a saved target. A company's stage or type is not a size.

## Example Usage

```typescript
import { PublicFindCompaniesEmployees } from "bereach/models/operations";

let value: PublicFindCompaniesEmployees = {};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `min`              | *number*           | :heavy_minus_sign: | N/A                |
| `max`              | *number*           | :heavy_minus_sign: | N/A                |