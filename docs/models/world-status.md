# WorldStatus

building while the build runs; ready when the World can be started; running or stopped once its Simulations exist; failed when the first start could not create its Simulations; canceled when the build was canceled.

## Example Usage

```typescript
import { WorldStatus } from "@continuous-labs/sdk/models";

let value: WorldStatus = "building";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"building" | "ready" | "running" | "stopped" | "failed" | "canceled" | Unrecognized<string>
```