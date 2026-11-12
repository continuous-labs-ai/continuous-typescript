# ListWebBoxSnapshotsResponse

## Example Usage

```typescript
import { ListWebBoxSnapshotsResponse } from "@continuous-labs/sdk/models";

let value: ListWebBoxSnapshotsResponse = {
  nextCursor: "<value>",
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
      createdAt: new Date("2025-11-03T20:53:19.559Z"),
      credentialIds: [],
      error: {
        agentMessage: "<value>",
        code: "build_canceled",
        detail: "<value>",
        reason: "service_unavailable",
        validation: {
          issues: [],
        },
      },
      hiddenLimitations: 66547,
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
      source: "build",
      sourceBoxId: "<id>",
      sourceSnapshotId: "<id>",
      status: "ready",
    },
  ],
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `nextCursor`                                             | *string*                                                 | :heavy_check_mark:                                       | Cursor for the next page, or null.                       |
| `snapshots`                                              | [models.WebBoxSnapshot](../models/web-box-snapshot.md)[] | :heavy_check_mark:                                       | Web Box Snapshots in this page.                          |