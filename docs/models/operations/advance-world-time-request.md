# AdvanceWorldTimeRequest

## Example Usage

```typescript
import { AdvanceWorldTimeRequest } from "@continuous-labs/sdk/models/operations";

let value: AdvanceWorldTimeRequest = {
  id: "<id>",
  idempotencyKey: "<value>",
  body: {
    to: new Date("2024-05-10T01:09:39.224Z"),
  },
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `id`                                                                                | *string*                                                                            | :heavy_check_mark:                                                                  | Simulation or World ID.                                                             |
| `idempotencyKey`                                                                    | *string*                                                                            | :heavy_check_mark:                                                                  | Stable key for this request. Reuse with the same target returns the same operation. |
| `body`                                                                              | [models.AdvanceTimeInputBody](../../models/advance-time-input-body.md)              | :heavy_check_mark:                                                                  | N/A                                                                                 |