# CreateSimulationRequest

## Example Usage

```typescript
import { CreateSimulationRequest } from "@continuous-labs/sdk/models";

let value: CreateSimulationRequest = {
  name: "billing-sandbox",
  simulatorId: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
};
```

## Fields

| Field                                                | Type                                                 | Required                                             | Description                                          |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `name`                                               | *string*                                             | :heavy_minus_sign:                                   | Optional Simulation name. Omission generates a name. |
| `simulatorId`                                        | *string*                                             | :heavy_check_mark:                                   | ID of the ready Simulator.                           |