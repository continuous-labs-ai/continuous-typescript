# APIBoxSnapshot

## Example Usage

```typescript
import { APIBoxSnapshot } from "@continuous-labs/sdk/models";

let value: APIBoxSnapshot = {
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
  createdAt: new Date("2025-03-23T00:09:40.497Z"),
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
  hiddenLimitations: 563483,
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
      reviewed: false,
    },
  ],
  metadata: "<value>",
  name: "<value>",
  research: {
    bytes: 359196,
    pages: 317014,
    status: "pending",
  },
  source: "catalog",
  specKind: "openapi",
  status: "canceled",
};
```

## Fields

| Field                                                                                                                                                                                                    | Type                                                                                                                                                                                                     | Required                                                                                                                                                                                                 | Description                                                                                                                                                                                              |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `build`                                                                                                                                                                                                  | [models.SimulatorBuildProgress](../models/simulator-build-progress.md)                                                                                                                                   | :heavy_check_mark:                                                                                                                                                                                       | The build's latest progress report, or null before the first report. A settled Snapshot keeps its last report. A build waiting for its live credentials resumes when the Snapshot's resume is requested. |
| `composition`                                                                                                                                                                                            | [models.SimulatorComposition](../models/simulator-composition.md)                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                                       | What a ready Snapshot serves, or null.                                                                                                                                                                   |
| `createdAt`                                                                                                                                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                                                            | :heavy_check_mark:                                                                                                                                                                                       | Snapshot creation time.                                                                                                                                                                                  |
| `credentialIds`                                                                                                                                                                                          | *string*[]                                                                                                                                                                                               | :heavy_check_mark:                                                                                                                                                                                       | Workspace credentials the build used, such as a web app login or credentials it was allowed to call real systems with. Empty when none.                                                                  |
| `error`                                                                                                                                                                                                  | [models.SimulatorError](../models/simulator-error.md)                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                                       | N/A                                                                                                                                                                                                      |
| `hiddenLimitations`                                                                                                                                                                                      | *number*                                                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                                       | Limitations the Snapshot records beyond those listed in limitations.                                                                                                                                     |
| `id`                                                                                                                                                                                                     | *string*                                                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                                       | API Box Snapshot ID.                                                                                                                                                                                     |
| `instructions`                                                                                                                                                                                           | *string*                                                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                                       | The instructions the build followed, or empty when none were given.                                                                                                                                      |
| `limitations`                                                                                                                                                                                            | [models.Limitation](../models/limitation.md)[]                                                                                                                                                           | :heavy_check_mark:                                                                                                                                                                                       | Behavior the Snapshot does not serve like the real system, most important first. Empty when none.                                                                                                        |
| `metadata`                                                                                                                                                                                               | *any*                                                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                                       | Customer JSON metadata, or null.                                                                                                                                                                         |
| `name`                                                                                                                                                                                                   | *string*                                                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                                       | Snapshot name. The ID is its identity, and names need not be unique.                                                                                                                                     |
| `research`                                                                                                                                                                                               | [models.SimulatorResearch](../models/simulator-research.md)                                                                                                                                              | :heavy_check_mark:                                                                                                                                                                                       | The build's research stage, or null when research did not run.                                                                                                                                           |
| `source`                                                                                                                                                                                                 | [models.APIBoxSnapshotSource](../models/api-box-snapshot-source.md)                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                                       | catalog for a Snapshot Continuous publishes, build for one built or published into the workspace, box for one saved from an API Box.                                                                     |
| `specKind`                                                                                                                                                                                               | [models.APIBoxSnapshotSpecKind](../models/api-box-snapshot-spec-kind.md)                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                                       | The specification the Snapshot was built from, or null until the build has read it.                                                                                                                      |
| `status`                                                                                                                                                                                                 | [models.APIBoxSnapshotStatus](../models/api-box-snapshot-status.md)                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                                       | pending while waiting for capacity; building while the build runs; ready when boxes can start from it; failed when the build failed; canceled when a cancel request took effect.                         |