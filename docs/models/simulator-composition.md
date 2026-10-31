# SimulatorComposition

## Example Usage

```typescript
import { SimulatorComposition } from "@continuous-labs/sdk/models";

let value: SimulatorComposition = {
  entities: 13542,
  operations: 229692,
  sample: false,
};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `entities`                                                                      | *number*                                                                        | :heavy_check_mark:                                                              | Entities that the Simulator stores.                                             |
| `operations`                                                                    | *number*                                                                        | :heavy_check_mark:                                                              | Operations that the Simulator routes.                                           |
| `sample`                                                                        | *boolean*                                                                       | :heavy_check_mark:                                                              | Whether the Simulator carries sample data that a new Simulation can start with. |