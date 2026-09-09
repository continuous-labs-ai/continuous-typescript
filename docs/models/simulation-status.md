# SimulationStatus

Current Simulation status.

## Example Usage

```typescript
import { SimulationStatus } from "@continuous-labs/sdk/models";

let value: SimulationStatus = "running";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"running" | "paused" | "stopped" | Unrecognized<string>
```