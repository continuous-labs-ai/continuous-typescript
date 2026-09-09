# Simulator

## Example Usage

```typescript
import { Simulator } from "@continuous-labs/sdk/models";

let value: Simulator = {
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

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Simulator creation time.                                                                      |
| `error`                                                                                       | [models.ResourceError](../models/resource-error.md)                                           | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Stable Simulator ID.                                                                          |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | Simulator name. Names cannot start with smr_.                                                 |
| `parentId`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | Stable parent Simulator ID, or null.                                                          |
| `source`                                                                                      | [models.Source](../models/source.md)                                                          | :heavy_check_mark:                                                                            | Simulator source.                                                                             |
| `status`                                                                                      | [models.SimulatorStatus](../models/simulator-status.md)                                       | :heavy_check_mark:                                                                            | Current build status.                                                                         |