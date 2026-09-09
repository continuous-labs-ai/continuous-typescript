# Simulation

## Example Usage

```typescript
import { Simulation } from "@continuous-labs/sdk/models";

let value: Simulation = {
  createdAt: new Date("2026-01-15T12:00:00Z"),
  endpoint: "https://api.continuouslabs.ai/sim/sim_01J8Z5X4K7M2N9P0Q1R2S3T4V6",
  id: "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V6",
  name: "billing-sandbox",
  parentId: "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V8",
  simulatorId: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
  status: "running",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Simulation creation time.                                                                     |
| `endpoint`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | Data-plane endpoint for the Simulation.                                                       |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Stable Simulation ID.                                                                         |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | Simulation name.                                                                              |
| `parentId`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | Stable source Simulation ID for a fork, or null.                                              |
| `simulatorId`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | Stable ID of the Simulator.                                                                   |
| `status`                                                                                      | [models.SimulationStatus](../models/simulation-status.md)                                     | :heavy_check_mark:                                                                            | Current Simulation status.                                                                    |