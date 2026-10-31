# MCPBoxSnapshot

## Example Usage

```typescript
import { MCPBoxSnapshot } from "@continuous-labs/sdk/models";

let value: MCPBoxSnapshot = {
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
  createdAt: new Date("2024-03-10T07:09:43.141Z"),
  credentialIds: [],
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
  sourceUrl: "https://abandoned-possession.net/",
  status: "failed",
};
```

## Fields

| Field                                                                                                                                                                                                       | Type                                                                                                                                                                                                        | Required                                                                                                                                                                                                    | Description                                                                                                                                                                                                 |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `apiboxSnapshotId`                                                                                                                                                                                          | *string*                                                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                                          | The API Box Snapshot the MCP Box was built against, whose API it calls.                                                                                                                                     |
| `build`                                                                                                                                                                                                     | [models.SimulatorBuildProgress](../models/simulator-build-progress.md)                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                                          | The build's latest progress report, or null before the first report. A settled Snapshot keeps its last report. A build waiting for its live credentials resumes with POST /v1/mcpbox-snapshots/{id}/resume. |
| `createdAt`                                                                                                                                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                                                               | :heavy_check_mark:                                                                                                                                                                                          | Snapshot creation time.                                                                                                                                                                                     |
| `credentialIds`                                                                                                                                                                                             | *string*[]                                                                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                                                          | Workspace credentials the build was allowed to call real systems with. Empty when none.                                                                                                                     |
| `error`                                                                                                                                                                                                     | [models.SimulatorError](../models/simulator-error.md)                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                                                          | N/A                                                                                                                                                                                                         |
| `id`                                                                                                                                                                                                        | *string*                                                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                                          | MCP Box Snapshot ID.                                                                                                                                                                                        |
| `instructions`                                                                                                                                                                                              | *string*                                                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                                          | The instructions the build followed, or empty when none were given.                                                                                                                                         |
| `metadata`                                                                                                                                                                                                  | *any*                                                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                                                          | Customer JSON metadata, or null.                                                                                                                                                                            |
| `name`                                                                                                                                                                                                      | *string*                                                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                                          | Snapshot name. The ID is its identity, and names need not be unique.                                                                                                                                        |
| `research`                                                                                                                                                                                                  | [models.SimulatorResearch](../models/simulator-research.md)                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                                          | The build's research stage, or null when research did not run.                                                                                                                                              |
| `sourceUrl`                                                                                                                                                                                                 | *string*                                                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                                          | The source MCP server whose tools the MCP Box serves, or empty when the build called no live source.                                                                                                        |
| `status`                                                                                                                                                                                                    | [models.MCPBoxSnapshotStatus](../models/mcp-box-snapshot-status.md)                                                                                                                                         | :heavy_check_mark:                                                                                                                                                                                          | pending while waiting for capacity; building while the build runs; ready when MCP Boxes can serve it; failed when the build failed; canceled when a cancel request took effect.                             |