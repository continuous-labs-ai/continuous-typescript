# CreatedSimulationStatus

Current status. starting means its runtime is booting; read the Simulation until it is running. running serves requests; after a period without requests, the first request can take longer while the Simulation resumes. stopping means its state is being saved, and stopped means it is saved; requests return 409 in both until you start it.

## Example Usage

```typescript
import { CreatedSimulationStatus } from "@continuous-labs/sdk/models";

let value: CreatedSimulationStatus = "starting";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"starting" | "running" | "stopping" | "stopped" | Unrecognized<string>
```