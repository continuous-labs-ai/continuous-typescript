# GetSimulationAdvanceRequest

## Example Usage

```typescript
import { GetSimulationAdvanceRequest } from "@continuous-labs/sdk/models/operations";

let value: GetSimulationAdvanceRequest = {
  id: "<id>",
  advanceId: "<id>",
};
```

## Fields

| Field                       | Type                        | Required                    | Description                 |
| --------------------------- | --------------------------- | --------------------------- | --------------------------- |
| `id`                        | *string*                    | :heavy_check_mark:          | Simulation or World ID.     |
| `advanceId`                 | *string*                    | :heavy_check_mark:          | Clock advance operation ID. |