# ListSimulationsResponse

## Example Usage

```typescript
import { ListSimulationsResponse } from "@continuous-labs/sdk/models";

let value: ListSimulationsResponse = {
  nextCursor: "<value>",
  simulations: [
    {
      createdAt: new Date("2026-01-15T12:00:00Z"),
      endpoint:
        "https://api.continuouslabs.ai/sim/sim_01J8Z5X4K7M2N9P0Q1R2S3T4V6",
      id: "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V6",
      name: "billing-sandbox",
      parentId: "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V8",
      simulatorId: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
      status: "running",
    },
  ],
};
```

## Fields

| Field                                          | Type                                           | Required                                       | Description                                    |
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| `nextCursor`                                   | *string*                                       | :heavy_check_mark:                             | Cursor for the next page, or null.             |
| `simulations`                                  | [models.Simulation](../models/simulation.md)[] | :heavy_check_mark:                             | Simulations in this page.                      |