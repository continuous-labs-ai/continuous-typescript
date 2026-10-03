# ListSimulatorsResponse

## Example Usage

```typescript
import { ListSimulatorsResponse } from "@continuous-labs/sdk/models";

let value: ListSimulatorsResponse = {
  nextCursor: null,
  simulators: [
    {
      build: {
        hiddenLimitations: 0,
        lastSubmission: "rejected",
        lastTool: "test",
        limitations: [],
        model: "claude-fable-5-1",
        phase: "build",
        stage: "build",
        submissions: 1,
        toolCalls: 7,
        warnings: [],
      },
      createdAt: new Date("2026-01-15T12:00:00Z"),
      error: null,
      id: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
      instructions: "Return stable example data for every operation.",
      name: "billing-api",
      parentId: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V9",
      source: "workspace",
      specKind: "openapi",
      status: "building",
    },
  ],
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `nextCursor`                                 | *string*                                     | :heavy_check_mark:                           | Cursor for the next page, or null.           |
| `simulators`                                 | [models.Simulator](../models/simulator.md)[] | :heavy_check_mark:                           | Simulators in this page.                     |