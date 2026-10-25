# CreateWorldAdvanceRequest

## Example Usage

```typescript
import { CreateWorldAdvanceRequest } from "@continuous-labs/sdk/models/operations";

let value: CreateWorldAdvanceRequest = {
  id: "<id>",
  idempotencyKey: "<value>",
  body: {
    to: new Date("2026-06-05T17:59:41.070Z"),
  },
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `id`                                                                                | *string*                                                                            | :heavy_check_mark:                                                                  | World ID.                                                                           |
| `idempotencyKey`                                                                    | *string*                                                                            | :heavy_check_mark:                                                                  | Stable key for this request. Reuse with the same target returns the same operation. |
| `body`                                                                              | [models.AdvanceTimeRequest](../../models/advance-time-request.md)                   | :heavy_check_mark:                                                                  | N/A                                                                                 |