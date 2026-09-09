# ListSimulationStepsRequest

## Example Usage

```typescript
import { ListSimulationStepsRequest } from "@continuous-labs/sdk/models/operations";

let value: ListSimulationStepsRequest = {
  id: "<id>",
};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `id`                                                        | *string*                                                    | :heavy_check_mark:                                          | Stable Simulation ID.                                       |
| `cursor`                                                    | *string*                                                    | :heavy_minus_sign:                                          | Opaque next_cursor value from a previous page.              |
| `limit`                                                     | *number*                                                    | :heavy_minus_sign:                                          | Page size. Values below 1 use 50. Values above 200 use 200. |