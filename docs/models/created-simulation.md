# CreatedSimulation

## Example Usage

```typescript
import { CreatedSimulation } from "@continuous-labs/sdk/models";

let value: CreatedSimulation = {
  createdAt: new Date("2026-01-15T12:00:00Z"),
  endpoint: "https://api.continuouslabs.ai/sim/sim_01J8Z5X4K7M2N9P0Q1R2S3T4V6",
  expiresAt: new Date("2026-01-15T13:00:00Z"),
  id: "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V6",
  name: "billing-sandbox",
  parentId: "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V8",
  simulatorId: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
  status: "running",
  token: "<redacted>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Simulation creation time.                                                                     |
| `endpoint`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | Data-plane endpoint for the Simulation.                                                       |
| `expiresAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Token expiration time.                                                                        |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Stable Simulation ID.                                                                         |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | Simulation name.                                                                              |
| `parentId`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | Stable source Simulation ID for a fork, or null.                                              |
| `simulatorId`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | Stable ID of the Simulator.                                                                   |
| `status`                                                                                      | [models.CreatedSimulationStatus](../models/created-simulation-status.md)                      | :heavy_check_mark:                                                                            | Current Simulation status.                                                                    |
| `token`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | One-time data-plane token.                                                                    |