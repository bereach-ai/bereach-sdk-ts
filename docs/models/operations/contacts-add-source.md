# ContactsAddSource

How this contact was found. Optional for organic creation (defaults to manual_import), required for campaign-based addition. Unknown values default to manual_import.

## Example Usage

```typescript
import { ContactsAddSource } from "bereach/models/operations";

let value: ContactsAddSource = "search_results";
```

## Values

```typescript
"likes" | "comments" | "reposts" | "posts" | "company_followers" | "search_results" | "manual_import" | "event_attendees" | "group_members" | "engagement_scraping" | "content_search" | "followers_mining" | "people_search" | "job_search" | "company_search" | "network_expansion" | "bulk_visit" | "inbound"
```