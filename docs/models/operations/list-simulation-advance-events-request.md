# ListSimulationAdvanceEventsRequest

## Example Usage

```typescript
import { ListSimulationAdvanceEventsRequest } from "@continuous-labs/sdk/models/operations";

let value: ListSimulationAdvanceEventsRequest = {
  id: "<id>",
  advanceId: "<id>",
};
```

## Fields

| Field                                                              | Type                                                               | Required                                                           | Description                                                        |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `id`                                                               | *string*                                                           | :heavy_check_mark:                                                 | Simulation ID.                                                     |
| `advanceId`                                                        | *string*                                                           | :heavy_check_mark:                                                 | Advance ID. A historical fork can read inherited runtime receipts. |
| `limit`                                                            | *number*                                                           | :heavy_minus_sign:                                                 | Page size. Values below 1 use 50. Values above 200 use 200.        |
| `cursor`                                                           | *string*                                                           | :heavy_minus_sign:                                                 | Opaque next_cursor value from a previous page.                     |