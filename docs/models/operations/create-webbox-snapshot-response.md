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
      hiddenLimitations: 905264,
      lastSubmission: "rejected",
      lastTool: "<value>",
      limitations: [
        {
          location: "<value>",
          message: "<value>",
          operations: [
            "<value 1>",
            "<value 2>",
            "<value 3>",
          ],
          reviewed: true,
        },
      ],
      model: "combined",
      phase: "repair",
      reviewRound: 190163,
      reviewRounds: 170650,
      stage: "assemble",
      submissions: 468781,
      toolCalls: 23888,
      waitedSeconds: 350029,
      waiting: {
        credentialIds: [],
        deadline: new Date("2026-12-17T12:44:55.990Z"),
        reason: "<value>",
        since: new Date("2026-04-02T03:17:18.732Z"),
        type: "live_credentials",
      },
      warnings: [
        {
          code: "spec.schema_limit",
          location: "<value>",
          message: "<value>",
          operations: [
            "<value 1>",
            "<value 2>",
          ],
        },
      ],
    },
    composition: {
      entities: 188689,
      operations: 295894,
      sample: false,
    },
    createdAt: new Date("2024-11-14T16:46:43.264Z"),
    credentialIds: [
      "<value 1>",
    ],
    error: {
      agentMessage: "<value>",
      code: "specification_validation_failed",
      detail: "<value>",
      reason: "specification_invalid",
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
          "<value 3>",
        ],
        reviewed: true,
      },
    ],
    metadata: "<value>",
    name: "<value>",
    parentId: "<id>",
    research: {
      bytes: 978994,
      pages: 244930,
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