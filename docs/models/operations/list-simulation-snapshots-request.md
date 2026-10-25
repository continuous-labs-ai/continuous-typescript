# ListSimulationSnapshotsRequest

## Example Usage

```typescript
import { ListSimulationSnapshotsRequest } from "@continuous-labs/sdk/models/operations";

let value: ListSimulationSnapshotsRequest = {};
```

## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `simulationId`                                                | *string*                                                      | :heavy_minus_sign:                                            | Optional filter for the Snapshots saved from this Simulation. |
| `limit`                                                       | *number*                                                      | :heavy_minus_sign:                                            | Page size. Values below 1 use 50. Values above 200 use 200.   |
| `cursor`                                                      | *string*                                                      | :heavy_minus_sign:                                            | Opaque next_cursor value from a previous page.                |