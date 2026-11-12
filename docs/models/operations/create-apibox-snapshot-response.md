# CreateApiboxSnapshotResponse

## Example Usage

```typescript
import { CreateApiboxSnapshotResponse } from "@continuous-labs/sdk/models/operations";

let value: CreateApiboxSnapshotResponse = {
  headers: {
    "key": [
      "<value 1>",
      "<value 2>",
      "<value 3>",
    ],
    "key1": [
      "<value 1>",
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
    createdAt: new Date("2024-05-28T06:16:53.136Z"),
    credentialIds: [
      "<value 1>",
      "<value 2>",
      "<value 3>",
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
    hiddenLimitations: 506521,
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
    source: "box",
    sourceBoxId: "<id>",
    sourceSnapshotId: "<id>",
    specKind: "wsdl",
    status: "ready",
  },
};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `headers`                                                 | Record<string, *string*[]>                                | :heavy_check_mark:                                        | N/A                                                       |
| `result`                                                  | [models.APIBoxSnapshot](../../models/api-box-snapshot.md) | :heavy_check_mark:                                        | N/A                                                       |