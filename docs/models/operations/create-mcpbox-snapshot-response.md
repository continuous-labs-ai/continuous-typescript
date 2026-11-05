# CreateMcpboxSnapshotResponse

## Example Usage

```typescript
import { CreateMcpboxSnapshotResponse } from "@continuous-labs/sdk/models/operations";

let value: CreateMcpboxSnapshotResponse = {
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
    apiboxSnapshotId: "<id>",
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
    createdAt: new Date("2026-10-11T03:39:21.722Z"),
    credentialIds: [
      "<value 1>",
      "<value 2>",
      "<value 3>",
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
    hiddenLimitations: 795918,
    id: "<id>",
    instructions: "<value>",
    limitations: [],
    metadata: "<value>",
    name: "<value>",
    parentId: "<id>",
    research: {
      bytes: 978994,
      pages: 244930,
      status: "provided",
    },
    source: "box",
    sourceBoxId: "<id>",
    sourceSnapshotId: "<id>",
    sourceUrl: "https://reckless-mousse.net/",
    status: "canceled",
  },
};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `headers`                                                 | Record<string, *string*[]>                                | :heavy_check_mark:                                        | N/A                                                       |
| `result`                                                  | [models.MCPBoxSnapshot](../../models/mcp-box-snapshot.md) | :heavy_check_mark:                                        | N/A                                                       |