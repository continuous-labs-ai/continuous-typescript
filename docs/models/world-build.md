# WorldBuild

## Example Usage

```typescript
import { WorldBuild } from "@continuous-labs/sdk/models";

let value: WorldBuild = {
  stage: "planning",
};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `builder`                                                                     | [models.WorldBuildBuilder](../models/world-build-builder.md)                  | :heavy_minus_sign:                                                            | Selected model provider. Absent for builds created before provider selection. |
| `lastSubmission`                                                              | [models.WorldBuildLastSubmission](../models/world-build-last-submission.md)   | :heavy_minus_sign:                                                            | Outcome of the most recent plan submission.                                   |
| `lastTool`                                                                    | *string*                                                                      | :heavy_minus_sign:                                                            | Name of the most recent tool. Tool arguments and output are private.          |
| `stage`                                                                       | [models.WorldBuildStage](../models/world-build-stage.md)                      | :heavy_check_mark:                                                            | Current phase of starting-data preparation.                                   |
| `submissions`                                                                 | *number*                                                                      | :heavy_minus_sign:                                                            | Number of submitted starting-data plans.                                      |
| `summary`                                                                     | [models.WorldDataSummary](../models/world-data-summary.md)                    | :heavy_minus_sign:                                                            | N/A                                                                           |
| `toolCalls`                                                                   | *number*                                                                      | :heavy_minus_sign:                                                            | Number of agent tool calls.                                                   |