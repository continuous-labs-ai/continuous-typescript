# SimulationStatus

Current status. running serves requests; after a period without requests, the first request can take longer while the Simulation resumes. stopped means its state is saved and requests return 409 until you start it.

## Example Usage

```typescript
import { SimulationStatus } from "@continuous-labs/sdk/models";

let value: SimulationStatus = "running";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"running" | "stopped" | Unrecognized<string>
```