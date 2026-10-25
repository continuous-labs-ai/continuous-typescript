# ListSimulationSnapshotsResponse

## Example Usage

```typescript
import { ListSimulationSnapshotsResponse } from "@continuous-labs/sdk/models";

let value: ListSimulationSnapshotsResponse = {
  nextCursor: "<value>",
  simulationSnapshots: [
    {
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
    },
  ],
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `nextCursor`                                                    | *string*                                                        | :heavy_check_mark:                                              | Cursor for the next page, or null.                              |
| `simulationSnapshots`                                           | [models.SimulationSnapshot](../models/simulation-snapshot.md)[] | :heavy_check_mark:                                              | Snapshots in this page.                                         |