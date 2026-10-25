# CreateSimulationSnapshotRequest

## Example Usage

```typescript
import { CreateSimulationSnapshotRequest } from "@continuous-labs/sdk/models";

let value: CreateSimulationSnapshotRequest = {
  name: "before-refund",
  simulationId: "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V6",
};
```

## Fields

| Field                                 | Type                                  | Required                              | Description                           |
| ------------------------------------- | ------------------------------------- | ------------------------------------- | ------------------------------------- |
| `name`                                | *string*                              | :heavy_check_mark:                    | Snapshot name.                        |
| `simulationId`                        | *string*                              | :heavy_check_mark:                    | ID of the running Simulation to save. |