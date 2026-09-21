# ReviewStatus

Status of the original independent review, not approval of later edits. Null before review.

## Example Usage

```typescript
import { ReviewStatus } from "@continuous-labs/sdk/models";

let value: ReviewStatus = "accepted";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"pending" | "accepted" | "rejected" | Unrecognized<string>
```