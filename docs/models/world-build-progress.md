# WorldBuildProgress

## Example Usage

```typescript
import { WorldBuildProgress } from "@continuous-labs/sdk/models";

let value: WorldBuildProgress = {
  builder: "claude",
  lastSubmission: "rejected",
  lastTool: null,
  lastValidationCode: "nested_proof",
  phase: "build",
  recentTools: [],
  reviewStatus: null,
  stage: "validating",
  submissions: 355176,
  summary: {
    assumptions: [
      "<value 1>",
    ],
    conditions: [],
    records: [],
    relationships: [
      "<value 1>",
      "<value 2>",
      "<value 3>",
    ],
  },
  tests: 926072,
  toolCalls: 543190,
};
```

## Fields

| Field                                                                                                                                 | Type                                                                                                                                  | Required                                                                                                                              | Description                                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| `builder`                                                                                                                             | [models.WorldBuildProgressBuilder](../models/world-build-progress-builder.md)                                                         | :heavy_check_mark:                                                                                                                    | Selected model provider, or null for a build created before provider selection.                                                       |
| `lastSubmission`                                                                                                                      | [models.WorldBuildProgressLastSubmission](../models/world-build-progress-last-submission.md)                                          | :heavy_check_mark:                                                                                                                    | Outcome of the most recent plan submission, or null.                                                                                  |
| `lastTool`                                                                                                                            | *string*                                                                                                                              | :heavy_check_mark:                                                                                                                    | Name of the most recent tool, or null. Tool arguments and output are private.                                                         |
| `lastValidationCode`                                                                                                                  | [models.LastValidationCode](../models/last-validation-code.md)                                                                        | :heavy_check_mark:                                                                                                                    | Fixed code for the latest validation finding. Null when no finding is available. Authored details stay private.                       |
| `phase`                                                                                                                               | [models.WorldBuildProgressPhase](../models/world-build-progress-phase.md)                                                             | :heavy_check_mark:                                                                                                                    | Agent phase: build for generation, review for the separate reviewer, finalize for author repair after review. Null when not recorded. |
| `recentTools`                                                                                                                         | [models.BuildToolCall](../models/build-tool-call.md)[]                                                                                | :heavy_check_mark:                                                                                                                    | The most recent tool calls, oldest first, at most 20.                                                                                 |
| `reviewStatus`                                                                                                                        | [models.ReviewStatus](../models/review-status.md)                                                                                     | :heavy_check_mark:                                                                                                                    | Status of the original independent review, not approval of later edits. Null before review.                                           |
| `stage`                                                                                                                               | [models.WorldBuildProgressStage](../models/world-build-progress-stage.md)                                                             | :heavy_check_mark:                                                                                                                    | Internal step of starting-data preparation.                                                                                           |
| `submissions`                                                                                                                         | *number*                                                                                                                              | :heavy_check_mark:                                                                                                                    | Number of distinct candidate plans submitted.                                                                                         |
| `summary`                                                                                                                             | [models.WorldDataSummary](../models/world-data-summary.md)                                                                            | :heavy_check_mark:                                                                                                                    | Verified starting data, or null before a completed build.                                                                             |
| `tests`                                                                                                                               | *number*                                                                                                                              | :heavy_check_mark:                                                                                                                    | Number of distinct candidate plans tested. Zero when not recorded.                                                                    |
| `toolCalls`                                                                                                                           | *number*                                                                                                                              | :heavy_check_mark:                                                                                                                    | Number of agent tool calls.                                                                                                           |