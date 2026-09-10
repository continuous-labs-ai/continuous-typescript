# SimulatorStatus

building while the build runs; ready when Simulations, Worlds, and incremental builds can use it; failed when the build failed; canceled when a cancel request took effect.

## Example Usage

```typescript
import { SimulatorStatus } from "@continuous-labs/sdk/models";

let value: SimulatorStatus = "canceled";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"building" | "ready" | "failed" | "canceled" | Unrecognized<string>
```