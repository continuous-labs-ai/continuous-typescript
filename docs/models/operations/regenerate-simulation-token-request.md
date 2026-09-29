# RegenerateSimulationTokenRequest

## Example Usage

```typescript
import { RegenerateSimulationTokenRequest } from "@continuous-labs/sdk/models/operations";

let value: RegenerateSimulationTokenRequest = {
  id: "<id>",
  idempotencyKey: "<value>",
};
```

## Fields

| Field                                     | Type                                      | Required                                  | Description                               |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| `id`                                      | *string*                                  | :heavy_check_mark:                        | Simulation ID.                            |
| `idempotencyKey`                          | *string*                                  | :heavy_check_mark:                        | Stable key for this regeneration request. |