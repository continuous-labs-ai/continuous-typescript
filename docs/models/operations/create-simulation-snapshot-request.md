# CreateSimulationSnapshotRequest

## Example Usage

```typescript
import { CreateSimulationSnapshotRequest } from "@continuous-labs/sdk/models/operations";

let value: CreateSimulationSnapshotRequest = {
  idempotencyKey: "<value>",
  body: {
    atStep: 42,
    name: "before-refund",
    simulationId: "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V6",
  },
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `idempotencyKey`                                                                              | *string*                                                                                      | :heavy_check_mark:                                                                            | Stable key for this request. A retry with the same key returns the original Snapshot.         |                                                                                               |
| `body`                                                                                        | [models.CreateSimulationSnapshotRequest](../../models/create-simulation-snapshot-request.md)  | :heavy_check_mark:                                                                            | N/A                                                                                           | {<br/>"at_step": 42,<br/>"name": "before-refund",<br/>"simulation_id": "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V6"<br/>} |