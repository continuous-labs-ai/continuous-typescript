# RemoveWorldSimulationRequest

## Example Usage

```typescript
import { RemoveWorldSimulationRequest } from "@continuous-labs/sdk/models/operations";

let value: RemoveWorldSimulationRequest = {
  id: "<id>",
  simulationId: "<id>",
  idempotencyKey: "<value>",
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `id`                                                                                   | *string*                                                                               | :heavy_check_mark:                                                                     | World ID.                                                                              |
| `simulationId`                                                                         | *string*                                                                               | :heavy_check_mark:                                                                     | ID of the member Simulation to remove.                                                 |
| `idempotencyKey`                                                                       | *string*                                                                               | :heavy_check_mark:                                                                     | Stable key for this request. Reuse with the same body returns the same change.         |
| `body`                                                                                 | [models.RemoveWorldSimulationRequest](../../models/remove-world-simulation-request.md) | :heavy_minus_sign:                                                                     | N/A                                                                                    |