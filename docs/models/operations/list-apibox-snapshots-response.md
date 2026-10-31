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
        composition: {
          entities: 748332,
          operations: 191531,
          sample: true,
        },
        createdAt: new Date("2024-11-20T07:12:42.749Z"),
        credentialIds: [
          "<value 1>",
          "<value 2>",
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
        hiddenLimitations: 633157,
        id: "<id>",
        instructions: "<value>",
        limitations: [],
        metadata: "<value>",
        name: "<value>",
        research: {
          bytes: 654632,
          pages: 640740,
          status: "running",
        },
        source: "build",
        specKind: null,
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