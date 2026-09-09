# ListSimulationsRequest

## Example Usage

```typescript
import { ListSimulationsRequest } from "@continuous-labs/sdk/models/operations";

let value: ListSimulationsRequest = {};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `status`                                                                               | [operations.ListSimulationsStatus](../../models/operations/list-simulations-status.md) | :heavy_minus_sign:                                                                     | Optional lifecycle status filter.                                                      |
| `simulatorId`                                                                          | *string*                                                                               | :heavy_minus_sign:                                                                     | Optional stable Simulator ID filter.                                                   |
| `limit`                                                                                | *number*                                                                               | :heavy_minus_sign:                                                                     | Page size. Values below 1 use 50. Values above 200 use 200.                            |
| `cursor`                                                                               | *string*                                                                               | :heavy_minus_sign:                                                                     | Opaque next_cursor value from a previous page.                                         |