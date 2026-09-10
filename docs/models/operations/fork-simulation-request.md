# ForkSimulationRequest

## Example Usage

```typescript
import { ForkSimulationRequest } from "@continuous-labs/sdk/models/operations";

let value: ForkSimulationRequest = {
  id: "<id>",
  body: {
    atStep: 42,
    name: "billing-fork",
  },
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             | Example                                                                 |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `id`                                                                    | *string*                                                                | :heavy_check_mark:                                                      | Source Simulation ID.                                                   |                                                                         |
| `body`                                                                  | [models.ForkSimulationRequest](../../models/fork-simulation-request.md) | :heavy_check_mark:                                                      | N/A                                                                     | {<br/>"at_step": 42,<br/>"name": "billing-fork"<br/>}                   |