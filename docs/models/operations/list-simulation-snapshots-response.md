# ListSimulationSnapshotsResponse

## Example Usage

```typescript
import { ListSimulationSnapshotsResponse } from "@continuous-labs/sdk/models/operations";

let value: ListSimulationSnapshotsResponse = {
  result: {
    nextCursor: "<value>",
    simulationSnapshots: [
      {
        atStep: 42,
        createdAt: new Date("2026-01-15T12:00:00Z"),
        currentTime: new Date("2024-01-03T00:00:00Z"),
        id: "sns_01J8Z5X4K7M2N9P0Q1R2S3T4VC",
        name: "before-refund",
        simulationId: "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V8",
        simulatorId: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
        startTime: new Date("2024-01-01T00:00:00Z"),
      },
    ],
  },
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `result`                                                                                     | [models.ListSimulationSnapshotsResponse](../../models/list-simulation-snapshots-response.md) | :heavy_check_mark:                                                                           | N/A                                                                                          |