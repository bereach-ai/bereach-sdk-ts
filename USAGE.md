<!-- Start SDK Example Usage [usage] -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.engagement.collectEngagers({
    postUrls: [
      "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    ],
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->