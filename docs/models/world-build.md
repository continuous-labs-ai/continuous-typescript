# WorldBuild

## Example Usage

```typescript
import { WorldBuild } from "@continuous-labs/sdk/models";

let value: WorldBuild = {
  stage: "planning",
};
```

## Fields

| Field                                                      | Type                                                       | Required                                                   | Description                                                |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| `stage`                                                    | [models.WorldBuildStage](../models/world-build-stage.md)   | :heavy_check_mark:                                         | Current phase of starting-data preparation.                |
| `summary`                                                  | [models.WorldDataSummary](../models/world-data-summary.md) | :heavy_minus_sign:                                         | N/A                                                        |