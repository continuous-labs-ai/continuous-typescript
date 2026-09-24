# WorldBuildProgress

## Example Usage

```typescript
import { WorldBuildProgress } from "@continuous-labs/sdk/models";

let value: WorldBuildProgress = {
  builder: "claude",
  lastSubmission: "rejected",
  lastTool: null,
  lastValidationCode: "nested_proof",
  model: "gpt-6-astra",
  phase: null,
  recentTools: [],
  reviewStatus: "accepted",
  stage: "reviewing",
  submissions: 409166,
  summary: {
    assumptions: [],
    conditions: [
      "<value 1>",
      "<value 2>",
      "<value 3>",
    ],
    records: [
      {
        count: 543190,
        entity: "<value>",
        memberIndex: 28794,
        simulatorId: "<id>",
      },
    ],
    relationships: [
      "<value 1>",
      "<value 2>",
    ],
  },
  tests: 519104,
  toolCalls: 728638,
};
```

## Fields

| Field                                                                                                                                                                     | Type                                                                                                                                                                      | Required                                                                                                                                                                  | Description                                                                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `builder`                                                                                                                                                                 | [models.WorldBuildProgressBuilder](../models/world-build-progress-builder.md)                                                                                             | :heavy_check_mark:                                                                                                                                                        | Selected model provider, or null for a build created before provider selection.                                                                                           |
| `lastSubmission`                                                                                                                                                          | [models.WorldBuildProgressLastSubmission](../models/world-build-progress-last-submission.md)                                                                              | :heavy_check_mark:                                                                                                                                                        | Outcome of the most recent plan submission, or null.                                                                                                                      |
| `lastTool`                                                                                                                                                                | *string*                                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                        | Name of the most recent tool, or null. Tool arguments and output are private.                                                                                             |
| `lastValidationCode`                                                                                                                                                      | [models.LastValidationCode](../models/last-validation-code.md)                                                                                                            | :heavy_check_mark:                                                                                                                                                        | Fixed code for the latest validation finding. Null when no finding is available. Authored details stay private.                                                           |
| `model`                                                                                                                                                                   | [models.WorldBuildProgressModel](../models/world-build-progress-model.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                        | The model the builder and reviewer run on, or null for a build created before provider selection. A build recorded before model selection reports its provider's default. |
| `phase`                                                                                                                                                                   | [models.WorldBuildProgressPhase](../models/world-build-progress-phase.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                        | Agent phase: build for generation, review for the separate reviewer, finalize for author repair after review. Null when not recorded.                                     |
| `recentTools`                                                                                                                                                             | [models.BuildToolCall](../models/build-tool-call.md)[]                                                                                                                    | :heavy_check_mark:                                                                                                                                                        | The most recent tool calls, oldest first, at most 20.                                                                                                                     |
| `reviewStatus`                                                                                                                                                            | [models.ReviewStatus](../models/review-status.md)                                                                                                                         | :heavy_check_mark:                                                                                                                                                        | Status of the original independent review, not approval of later edits. Null before review.                                                                               |
| `stage`                                                                                                                                                                   | [models.WorldBuildProgressStage](../models/world-build-progress-stage.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                        | Internal step of starting-data preparation.                                                                                                                               |
| `submissions`                                                                                                                                                             | *number*                                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                        | Number of distinct candidate plans submitted.                                                                                                                             |
| `summary`                                                                                                                                                                 | [models.WorldDataSummary](../models/world-data-summary.md)                                                                                                                | :heavy_check_mark:                                                                                                                                                        | Verified starting data, or null before a completed build.                                                                                                                 |
| `tests`                                                                                                                                                                   | *number*                                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                        | Number of distinct candidate plans tested. Zero when not recorded.                                                                                                        |
| `toolCalls`                                                                                                                                                               | *number*                                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                        | Number of agent tool calls.                                                                                                                                               |