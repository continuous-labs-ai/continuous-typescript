# ListApiboxSnapshotsResponse

## Example Usage

```typescript
import { ListApiboxSnapshotsResponse } from "@continuous-labs/sdk/models/operations";

let value: ListApiboxSnapshotsResponse = {
  result: {
    nextCursor: null,
    snapshots: [
      {
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
        createdAt: new Date("2024-07-25T19:17:00.582Z"),
        credentialIds: [
          "<value 1>",
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
        hiddenLimitations: 515639,
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
        status: "pending",
      },
    ],
  },
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `result`                                                                              | [models.ListAPIBoxSnapshotsResponse](../../models/list-api-box-snapshots-response.md) | :heavy_check_mark:                                                                    | N/A                                                                                   |