# WorldChange

## Example Usage

```typescript
import { WorldChange } from "@continuous-labs/sdk/models";

let value: WorldChange = {
  completedAt: null,
  createdAt: new Date("2026-01-15T12:00:00Z"),
  delete: false,
  error: null,
  id: "wch_01J8Z5X4K7M2N9P0Q1R2S3T4VB",
  kind: "add",
  simulation: {
    id: "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V6",
    simulatorId: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
  },
  status: "applying",
  worldId: "wld_01J8Z5X4K7M2N9P0Q1R2S3T4V7",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `completedAt`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Time the change completed or failed, or null while it runs.                                   |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Change creation time.                                                                         |
| `delete`                                                                                      | *boolean*                                                                                     | :heavy_check_mark:                                                                            | Whether a removed member is deleted rather than detached.                                     |
| `error`                                                                                       | [models.ResourceError](../models/resource-error.md)                                           | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Membership change ID.                                                                         |
| `kind`                                                                                        | [models.WorldChangeKind](../models/world-change-kind.md)                                      | :heavy_check_mark:                                                                            | add adds a member; remove detaches or deletes one.                                            |
| `simulation`                                                                                  | [models.WorldSimulation](../models/world-simulation.md)                                       | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `status`                                                                                      | [models.WorldChangeStatus](../models/world-change-status.md)                                  | :heavy_check_mark:                                                                            | Durable change state. Poll while pending, building, or applying.                              |
| `worldId`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | World ID.                                                                                     |