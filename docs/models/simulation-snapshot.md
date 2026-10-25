# SimulationSnapshot

## Example Usage

```typescript
import { SimulationSnapshot } from "@continuous-labs/sdk/models";

let value: SimulationSnapshot = {
  createdAt: new Date("2026-01-15T12:00:00Z"),
  currentTime: new Date("2024-01-03T00:00:00Z"),
  error: null,
  id: "sns_01J8Z5X4K7M2N9P0Q1R2S3T4VC",
  name: "before-refund",
  simulationId: "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V8",
  simulationName: "checkout-run",
  simulatorId: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
  startTime: new Date("2024-01-01T00:00:00Z"),
  status: "ready",
};
```

## Fields

| Field                                                                                                              | Type                                                                                                               | Required                                                                                                           | Description                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| `createdAt`                                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                      | :heavy_check_mark:                                                                                                 | Snapshot creation time.                                                                                            |
| `currentTime`                                                                                                      | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                      | :heavy_check_mark:                                                                                                 | Simulated time of the saved state, where a Simulation created from the Snapshot starts, or null until it is ready. |
| `error`                                                                                                            | [models.ResourceError](../models/resource-error.md)                                                                | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `id`                                                                                                               | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | Snapshot ID.                                                                                                       |
| `name`                                                                                                             | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | Snapshot name. The ID is its identity, and names need not be unique.                                               |
| `simulationId`                                                                                                     | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | ID of the Simulation the Snapshot saved, or null once that Simulation is deleted.                                  |
| `simulationName`                                                                                                   | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | Current name of the Simulation the Snapshot saved, or null once that Simulation is deleted.                        |
| `simulatorId`                                                                                                      | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | ID of the Simulator a Simulation created from the Snapshot runs, at the digest its source pinned.                  |
| `startTime`                                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                      | :heavy_check_mark:                                                                                                 | Initial simulated time of a Simulation created from the Snapshot, or null until it is ready.                       |
| `status`                                                                                                           | [models.SimulationSnapshotStatus](../models/simulation-snapshot-status.md)                                         | :heavy_check_mark:                                                                                                 | creating while the state is saved. A Simulation can start from a ready Snapshot. A failed Snapshot holds no state. |