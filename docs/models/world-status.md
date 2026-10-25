# WorldStatus

pending while waiting for capacity; building while the build runs; ready when it can be started; starting while its Simulations start; running or stopped once its Simulations exist; stopping while they stop; failed when building or first start fails; canceled when the build was canceled.

## Example Usage

```typescript
import { WorldStatus } from "@continuous-labs/sdk/models";

let value: WorldStatus = "building";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"pending" | "building" | "ready" | "starting" | "running" | "stopping" | "stopped" | "failed" | "canceled" | Unrecognized<string>
```