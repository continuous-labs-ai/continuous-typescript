# ListSimulationStepsResponse

## Example Usage

```typescript
import { ListSimulationStepsResponse } from "@continuous-labs/sdk/models";

let value: ListSimulationStepsResponse = {
  nextCursor: "<value>",
  steps: [],
};
```

## Fields

| Field                              | Type                               | Required                           | Description                        |
| ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- |
| `nextCursor`                       | *string*                           | :heavy_check_mark:                 | Cursor for the next page, or null. |
| `steps`                            | [models.Step](../models/step.md)[] | :heavy_check_mark:                 | Recorded steps in this page.       |