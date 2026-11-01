# CreateApiboxSnapshotResponse

## Example Usage

```typescript
import { CreateApiboxSnapshotResponse } from "@continuous-labs/sdk/models/operations";

let value: CreateApiboxSnapshotResponse = {
  headers: {},
  result: {
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
        type: "time_limit",
      },
      warnings: [],
    },
    composition: {
      entities: 586913,
      operations: 748332,
      sample: true,
    },
    createdAt: new Date("2025-06-29T16:02:36.926Z"),
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
        issues: [
          {
            code: "<value>",
            kind: "unsupported",
            location: "<value>",
            message: "<value>",
            operation: "<value>",
            suggestion: "<value>",
          },
        ],
      },
    },
    hiddenLimitations: 976454,
    id: "<id>",
    instructions: "<value>",
    limitations: [],
    metadata: "<value>",
    name: "<value>",
    research: {
      bytes: 359196,
      pages: 317014,
      status: "pending",
    },
    source: "box",
    specKind: "graphql",
    status: "ready",
  },
};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `headers`                                                 | Record<string, *string*[]>                                | :heavy_check_mark:                                        | N/A                                                       |
| `result`                                                  | [models.APIBoxSnapshot](../../models/api-box-snapshot.md) | :heavy_check_mark:                                        | N/A                                                       |