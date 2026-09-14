# WorldStatus

pending while waiting for capacity; building while the build runs; ready when it can be started; running or stopped once its Simulations exist; failed when building or first start fails; canceled when the build was canceled.

## Example Usage

```typescript
import { WorldStatus } from "@continuous-labs/sdk/models";

let value: WorldStatus = "building";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"pending" | "building" | "ready" | "running" | "stopped" | "failed" | "canceled" | Unrecognized<string>
```