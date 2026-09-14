# WorldBuildProgress

## Example Usage

```typescript
import { WorldBuildProgress } from "@continuous-labs/sdk/models";

let value: WorldBuildProgress = {
  builder: "claude",
  lastSubmission: "rejected",
  lastTool: null,
  recentTools: [
    {
      at: new Date("2025-08-10T11:22:23.230Z"),
      tool: "<value>",
    },
  ],
  stage: "complete",
  submissions: 181836,
  summary: null,
  toolCalls: 86959,
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `builder`                                                                                    | [models.WorldBuildProgressBuilder](../models/world-build-progress-builder.md)                | :heavy_check_mark:                                                                           | Selected model provider, or null for a build created before provider selection.              |
| `lastSubmission`                                                                             | [models.WorldBuildProgressLastSubmission](../models/world-build-progress-last-submission.md) | :heavy_check_mark:                                                                           | Outcome of the most recent plan submission, or null.                                         |
| `lastTool`                                                                                   | *string*                                                                                     | :heavy_check_mark:                                                                           | Name of the most recent tool, or null. Tool arguments and output are private.                |
| `recentTools`                                                                                | [models.BuildToolCall](../models/build-tool-call.md)[]                                       | :heavy_check_mark:                                                                           | The most recent tool calls, oldest first, at most 20.                                        |
| `stage`                                                                                      | [models.WorldBuildProgressStage](../models/world-build-progress-stage.md)                    | :heavy_check_mark:                                                                           | Current phase of starting-data preparation.                                                  |
| `submissions`                                                                                | *number*                                                                                     | :heavy_check_mark:                                                                           | Number of submitted starting-data plans.                                                     |
| `summary`                                                                                    | [models.WorldDataSummary](../models/world-data-summary.md)                                   | :heavy_check_mark:                                                                           | Verified starting data, or null before a completed build.                                    |
| `toolCalls`                                                                                  | *number*                                                                                     | :heavy_check_mark:                                                                           | Number of agent tool calls.                                                                  |