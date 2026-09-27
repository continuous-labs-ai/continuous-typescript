# AdvanceSimulationRequest

## Example Usage

```typescript
import { AdvanceSimulationRequest } from "@continuous-labs/sdk/models/operations";

let value: AdvanceSimulationRequest = {
  id: "<id>",
  idempotencyKey: "<value>",
  body: {
    to: new Date("2024-08-31T04:41:49.911Z"),
  },
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `id`                                                                                | *string*                                                                            | :heavy_check_mark:                                                                  | Simulation ID.                                                                      |
| `idempotencyKey`                                                                    | *string*                                                                            | :heavy_check_mark:                                                                  | Stable key for this request. Reuse with the same target returns the same operation. |
| `body`                                                                              | [models.AdvanceTimeRequest](../../models/advance-time-request.md)                   | :heavy_check_mark:                                                                  | N/A                                                                                 |