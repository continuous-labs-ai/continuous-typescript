# ListSimulatorsResponse

## Example Usage

```typescript
import { ListSimulatorsResponse } from "@continuous-labs/sdk/models/operations";

let value: ListSimulatorsResponse = {
  result: {
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
          reviewRound: 0,
          reviewRounds: 1,
          stage: "build",
          submissions: 1,
          toolCalls: 7,
          waitedSeconds: 0,
          waiting: null,
          warnings: [],
        },
        createdAt: new Date("2026-01-15T12:00:00Z"),
        credentialIds: [],
        error: null,
        id: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
        instructions: "Return stable example data for every operation.",
        mode: "api",
        name: "billing-api",
        parentId: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V9",
        publication: null,
        research: null,
        source: "workspace",
        specKind: "openapi",
        status: "building",
      },
    ],
  },
};
```

## Fields

| Field                                                                     | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `result`                                                                  | [models.ListSimulatorsResponse](../../models/list-simulators-response.md) | :heavy_check_mark:                                                        | N/A                                                                       |