# SimulationSnapshotStatus

creating while the state is saved. A Simulation can start from a ready Snapshot. A failed Snapshot holds no state.

## Example Usage

```typescript
import { SimulationSnapshotStatus } from "@continuous-labs/sdk/models";

let value: SimulationSnapshotStatus = "failed";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"creating" | "ready" | "failed" | Unrecognized<string>
```