# CreateWebboxSnapshotResponse

## Example Usage

```typescript
import { CreateWebboxSnapshotResponse } from "@continuous-labs/sdk/models/operations";

let value: CreateWebboxSnapshotResponse = {
  headers: {
    "key": [
      "<value 1>",
      "<value 2>",
    ],
  },
  result: {
    actors: [
      {
        default: false,
        entity: "<value>",
        id: "<id>",
        name: "<value>",
        role: "<value>",
      },
    ],
    build: {
      agentState: "<value>",
      hiddenLimitations: 999940,
      lastActivityAt: new Date("2025-07-03T07:22:21.692Z"),
      lastSubmission: "<value>",
      lastTool: "<value>",
      limitations: [],
      model: "combined",
      phase: "<value>",
      reviewRound: 931544,
      reviewRounds: 190163,
      stage: "<value>",
      submissions: 170650,
      toolCalls: 992879,
      waitedSeconds: 468781,
      waiting: null,
      waitingUntil: new Date("2024-07-22T22:01:08.071Z"),
      warnings: [],
    },
    composition: {
      entities: 750125,
      operations: 394300,
      sample: false,
    },
    createdAt: new Date("2024-11-14T16:46:43.264Z"),
    credentialIds: [
      "<value 1>",
    ],
    error: {
      agentMessage: "<value>",
      code: "build_canceled",
      detail: "<value>",
      reason: "service_unavailable",
      validation: {
        issues: [],
      },
    },
    hiddenLimitations: 65108,
    id: "<id>",
    instructions: "<value>",
    limitations: [
      {
        location: "<value>",
        message: "<value>",
        operations: [
          "<value 1>",
          "<value 2>",
        ],
        reviewed: true,
      },
    ],
    metadata: "<value>",
    name: "<value>",
    parentId: "<id>",
    research: {
      bytes: 509538,
      pages: 124429,
      status: "provided",
    },
    source: "catalog",
    sourceBoxId: "<id>",
    sourceSnapshotId: "<id>",
    status: "ready",
  },
};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `headers`                                                 | Record<string, *string*[]>                                | :heavy_check_mark:                                        | N/A                                                       |
| `result`                                                  | [models.WebBoxSnapshot](../../models/web-box-snapshot.md) | :heavy_check_mark:                                        | N/A                                                       |