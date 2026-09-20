# WorldErrorReason

Bounded failure reason for selecting recovery guidance, or null when unavailable. Older servers can omit this field.

## Example Usage

```typescript
import { WorldErrorReason } from "@continuous-labs/sdk/models";

let value: WorldErrorReason = "build_failed";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"canceled" | "specification_invalid" | "time_limit" | "service_unavailable" | "build_failed" | "population_unsupported" | "world_start_failed" | "world_operation_failed" | Unrecognized<string>
```