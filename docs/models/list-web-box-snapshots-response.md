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
        agentState: "waiting_for_limit",
        hiddenLimitations: 852380,
        lastActivityAt: new Date("2026-01-07T20:02:24.666Z"),
        lastSubmission: "accepted",
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
        model: "gpt-6.1-sol",
        phase: "review",
        reviewRound: 23888,
        reviewRounds: 350029,
        stage: "derive",
        submissions: 147908,
        toolCalls: 986799,
        waitedSeconds: 750125,
        waiting: {
          credentialIds: [
            "<value 1>",
            "<value 2>",
            "<value 3>",
          ],
          deadline: new Date("2025-10-05T06:09:26.950Z"),
          reason: "<value>",
          since: new Date("2026-03-31T04:06:20.010Z"),
          type: "live_credentials",
        },
        waitingUntil: new Date("2024-11-20T07:12:42.749Z"),
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
        entities: 371076,
        operations: 654632,
        sample: false,
      },
      createdAt: new Date("2025-11-03T20:53:19.559Z"),
      credentialIds: [],
      error: {
        agentMessage: "<value>",
        code: "live_credential_rejected",
        detail: "<value>",
        reason: "build_failed",
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