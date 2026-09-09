# World

## Example Usage

```typescript
import { World } from "@continuous-labs/sdk/models";

let value: World = {
  createdAt: new Date("2026-01-15T12:00:00Z"),
  error: null,
  id: "wld_01J8Z5X4K7M2N9P0Q1R2S3T4V7",
  instructions: "Use stable example data for each Simulator.",
  simulations: [],
  simulators: [
    "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
  ],
  status: "building",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Time when the World build started.                                                            |
| `error`                                                                                       | [models.ResourceError](../models/resource-error.md)                                           | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Stable World ID.                                                                              |
| `instructions`                                                                                | *string*                                                                                      | :heavy_check_mark:                                                                            | Build guidance stored with the World.                                                         |
| `simulations`                                                                                 | [models.WorldSimulation](../models/world-simulation.md)[]                                     | :heavy_check_mark:                                                                            | Created member Simulations. This list is empty before first start.                            |
| `simulators`                                                                                  | *string*[]                                                                                    | :heavy_check_mark:                                                                            | Stable Simulator IDs in member order.                                                         |
| `status`                                                                                      | [models.WorldStatus](../models/world-status.md)                                               | :heavy_check_mark:                                                                            | Current World lifecycle status.                                                               |