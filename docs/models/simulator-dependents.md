# SimulatorDependents

## Example Usage

```typescript
import { SimulatorDependents } from "@continuous-labs/sdk/models";

let value: SimulatorDependents = {
  childSimulators: [
    "<value 1>",
    "<value 2>",
  ],
  simulations: [
    "<value 1>",
    "<value 2>",
  ],
  snapshots: [],
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `childSimulators`                                                      | *string*[]                                                             | :heavy_check_mark:                                                     | IDs of Simulators built from the Simulator.                            |
| `simulations`                                                          | *string*[]                                                             | :heavy_check_mark:                                                     | IDs of Simulations created from the Simulator.                         |
| `snapshots`                                                            | *string*[]                                                             | :heavy_check_mark:                                                     | IDs of Simulation Snapshots of Simulations created from the Simulator. |