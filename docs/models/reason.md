# Reason

Bounded failure reason for selecting recovery guidance, or null when unavailable.

## Example Usage

```typescript
import { Reason } from "@continuous-labs/sdk/models";

let value: Reason = "build_failed";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"canceled" | "specification_invalid" | "time_limit" | "service_unavailable" | "build_failed" | Unrecognized<string>
```