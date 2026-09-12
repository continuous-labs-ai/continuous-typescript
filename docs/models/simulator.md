# Simulator

## Example Usage

```typescript
import { Simulator } from "@continuous-labs/sdk/models";

let value: Simulator = {
  build: {
    builder: "claude",
    lastSubmission: "rejected",
    lastTool: "test",
    stage: "build",
    submissions: 1,
    toolCalls: 7,
    updatedAt: new Date("2026-01-15T12:05:00Z"),
  },
  createdAt: new Date("2026-01-15T12:00:00Z"),
  error: null,
  id: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
  name: "billing-api",
  parentId: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V9",
  source: "workspace",
  status: "building",
};
```

## Fields

| Field                                                                                                                                                                       | Type                                                                                                                                                                        | Required                                                                                                                                                                    | Description                                                                                                                                                                 |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `build`                                                                                                                                                                     | [models.SimulatorBuildProgress](../models/simulator-build-progress.md)                                                                                                      | :heavy_check_mark:                                                                                                                                                          | The build's latest progress report, or null before the first report. A terminal Simulator keeps its last report.                                                            |
| `createdAt`                                                                                                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                               | :heavy_check_mark:                                                                                                                                                          | Simulator creation time.                                                                                                                                                    |
| `error`                                                                                                                                                                     | [models.SimulatorError](../models/simulator-error.md)                                                                                                                       | :heavy_check_mark:                                                                                                                                                          | N/A                                                                                                                                                                         |
| `id`                                                                                                                                                                        | *string*                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                          | Simulator ID.                                                                                                                                                               |
| `name`                                                                                                                                                                      | *string*                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                          | Simulator name. Names cannot start with smr_.                                                                                                                               |
| `parentId`                                                                                                                                                                  | *string*                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                          | Parent Simulator ID, or null.                                                                                                                                               |
| `source`                                                                                                                                                                    | [models.Source](../models/source.md)                                                                                                                                        | :heavy_check_mark:                                                                                                                                                          | workspace for a Simulator your workspace built; catalog for a read-only Simulator that Continuous publishes.                                                                |
| `status`                                                                                                                                                                    | [models.SimulatorStatus](../models/simulator-status.md)                                                                                                                     | :heavy_check_mark:                                                                                                                                                          | building while the build runs; ready when Simulations, Worlds, and incremental builds can use it; failed when the build failed; canceled when a cancel request took effect. |