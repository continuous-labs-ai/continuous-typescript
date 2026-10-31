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
    "key1": [],
    "key2": [],
  },
  result: {
    apiboxSnapshotId: "<id>",
    build: {
      hiddenLimitations: 761235,
      lastSubmission: "rejected",
      lastTool: "<value>",
      limitations: [
        {
          location: "<value>",
          message: "<value>",
          operations: [
            "<value 1>",
            "<value 2>",
          ],
          reviewed: false,
        },
      ],
      model: "gpt-6.1-sol",
      phase: "review",
      reviewRound: 931544,
      reviewRounds: 190163,
      stage: "derive",
      submissions: 992879,
      toolCalls: 468781,
      waitedSeconds: 23888,
      waiting: {
        credentialIds: [],
        deadline: new Date("2024-06-11T02:34:42.777Z"),
        reason: "<value>",
        since: new Date("2026-12-17T12:44:55.990Z"),
      },
      warnings: [
        {
          code: "spec.default_invalid",
          location: "<value>",
          message: "<value>",
          operations: [
            "<value 1>",
            "<value 2>",
            "<value 3>",
          ],
        },
      ],
    },
    createdAt: new Date("2024-09-11T19:59:47.135Z"),
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
    id: "<id>",
    instructions: "<value>",
    metadata: "<value>",
    name: "<value>",
    research: {
      bytes: 654632,
      pages: 640740,
      status: "running",
    },
    sourceUrl: "https://stale-kick.net",
    status: "canceled",
  },
};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `headers`                                                 | Record<string, *string*[]>                                | :heavy_check_mark:                                        | N/A                                                       |
| `result`                                                  | [models.MCPBoxSnapshot](../../models/mcp-box-snapshot.md) | :heavy_check_mark:                                        | N/A                                                       |