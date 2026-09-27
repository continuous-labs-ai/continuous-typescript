# SimulatorErrorReason

Bounded failure reason for selecting recovery guidance, or null when unavailable.

## Example Usage

```typescript
import { SimulatorErrorReason } from "@continuous-labs/sdk/models";

let value: SimulatorErrorReason = "build_failed";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"canceled" | "specification_invalid" | "time_limit" | "service_unavailable" | "build_failed" | Unrecognized<string>
```