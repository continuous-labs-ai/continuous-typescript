# WorldSimulation

## Example Usage

```typescript
import { WorldSimulation } from "@continuous-labs/sdk/models";

let value: WorldSimulation = {
  id: "<id>",
  simulatorId: "<id>",
};
```

## Fields

| Field                                          | Type                                           | Required                                       | Description                                    |
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| `id`                                           | *string*                                       | :heavy_check_mark:                             | ID of the created Simulation.                  |
| `simulatorId`                                  | *string*                                       | :heavy_check_mark:                             | ID of the Simulator that this Simulation runs. |