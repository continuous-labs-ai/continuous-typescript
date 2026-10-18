# SimulatorPublicationStatus

published once the Simulator's image is in the environment's own registry; failed when the last attempt failed. Creating a Simulation in the environment tries again.

## Example Usage

```typescript
import { SimulatorPublicationStatus } from "@continuous-labs/sdk/models";

let value: SimulatorPublicationStatus = "failed";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"published" | "failed" | Unrecognized<string>
```