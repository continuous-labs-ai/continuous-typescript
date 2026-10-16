# AddWorldSimulationRequest

## Example Usage

```typescript
import { AddWorldSimulationRequest } from "@continuous-labs/sdk/models/operations";

let value: AddWorldSimulationRequest = {
  id: "<id>",
  idempotencyKey: "<value>",
  body: {
    simulator: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
  },
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      | Example                                                                          |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `id`                                                                             | *string*                                                                         | :heavy_check_mark:                                                               | World ID.                                                                        |                                                                                  |
| `idempotencyKey`                                                                 | *string*                                                                         | :heavy_check_mark:                                                               | Stable key for this request. Reuse with the same body returns the same change.   |                                                                                  |
| `body`                                                                           | [models.AddWorldSimulationRequest](../../models/add-world-simulation-request.md) | :heavy_check_mark:                                                               | N/A                                                                              | {<br/>"simulator": "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5"<br/>}                        |