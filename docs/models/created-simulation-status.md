# CreatedSimulationStatus

Current status. running serves requests. paused means the Simulation was idle and the platform paused it; the next request wakes it. stopped means its state is saved and requests return 409 until you start it.

## Example Usage

```typescript
import { CreatedSimulationStatus } from "@continuous-labs/sdk/models";

let value: CreatedSimulationStatus = "running";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"running" | "paused" | "stopped" | Unrecognized<string>
```