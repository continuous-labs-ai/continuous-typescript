# SimulationDetailStatus

Current status. running serves requests. paused means the Simulation was idle and the platform paused it; the next request wakes it. stopped means its state is saved and requests return 409 until you start it.

## Example Usage

```typescript
import { SimulationDetailStatus } from "@continuous-labs/sdk/models";

let value: SimulationDetailStatus = "running";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"running" | "paused" | "stopped" | Unrecognized<string>
```