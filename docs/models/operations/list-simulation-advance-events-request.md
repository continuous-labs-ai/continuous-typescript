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
| `cursor`                                                           | *string*                                                           | :heavy_minus_sign:                                                 | Cursor from the previous page.                                     |
| `limit`                                                            | *number*                                                           | :heavy_minus_sign:                                                 | Page size, up to 200.                                              |