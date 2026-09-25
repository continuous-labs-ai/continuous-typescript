# CreateSimulationRequest

## Example Usage

```typescript
import { CreateSimulationRequest } from "@continuous-labs/sdk/models";

let value: CreateSimulationRequest = {
  metadata: {
    "customer_id": "cust_123",
  },
  name: "billing-sandbox",
  simulatorId: "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
};
```

## Fields

| Field                                                                                                              | Type                                                                                                               | Required                                                                                                           | Description                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| `metadata`                                                                                                         | *any*                                                                                                              | :heavy_minus_sign:                                                                                                 | Customer JSON metadata, up to 16 KiB and 64 nesting levels. Returned by create, get, and list. Omission uses null. |
| `name`                                                                                                             | *string*                                                                                                           | :heavy_minus_sign:                                                                                                 | Name for the Simulation. Omission generates a name. The ID stays its identity, and names need not be unique.       |
| `simulatorId`                                                                                                      | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | ID of the ready Simulator.                                                                                         |
| `startTime`                                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                      | :heavy_minus_sign:                                                                                                 | Initial simulated time in RFC 3339 format. Omission uses 2024-01-01T00:00:00Z. Precision is milliseconds.          |