# CreateSimulationSnapshotRequest

## Example Usage

```typescript
import { CreateSimulationSnapshotRequest } from "@continuous-labs/sdk/models";

let value: CreateSimulationSnapshotRequest = {
  atStep: 42,
  name: "before-refund",
  simulationId: "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V6",
};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `atStep`                                                                 | *number*                                                                 | :heavy_minus_sign:                                                       | Completed step to save the state after. Omission saves the latest state. |
| `name`                                                                   | *string*                                                                 | :heavy_check_mark:                                                       | Snapshot name.                                                           |
| `simulationId`                                                           | *string*                                                                 | :heavy_check_mark:                                                       | ID of the running Simulation to save.                                    |