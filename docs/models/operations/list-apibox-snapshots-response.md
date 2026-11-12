# ListApiboxSnapshotsResponse

## Example Usage

```typescript
import { ListApiboxSnapshotsResponse } from "@continuous-labs/sdk/models/operations";

let value: ListApiboxSnapshotsResponse = {
  result: {
    nextCursor: null,
    snapshots: [
      {
        actors: [],
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
        createdAt: new Date("2025-10-05T06:09:26.950Z"),
        credentialIds: [
          "<value 1>",
          "<value 2>",
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
        hiddenLimitations: 371076,
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
        research: null,
        source: "catalog",
        sourceBoxId: "<id>",
        sourceSnapshotId: "<id>",
        specKind: "graphql",
        status: "building",
      },
    ],
  },
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `result`                                                                              | [models.ListAPIBoxSnapshotsResponse](../../models/list-api-box-snapshots-response.md) | :heavy_check_mark:                                                                    | N/A                                                                                   |