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

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `name`                                                                                                    | *string*                                                                                                  | :heavy_minus_sign:                                                                                        | Optional Simulation name. Omission generates a name.                                                      |
| `simulatorId`                                                                                             | *string*                                                                                                  | :heavy_check_mark:                                                                                        | ID of the ready Simulator.                                                                                |
| `startTime`                                                                                               | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)             | :heavy_minus_sign:                                                                                        | Initial simulated time in RFC 3339 format. Omission uses 2024-01-01T00:00:00Z. Precision is milliseconds. |