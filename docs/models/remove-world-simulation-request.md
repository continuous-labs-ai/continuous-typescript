# RemoveWorldSimulationRequest

## Example Usage

```typescript
import { RemoveWorldSimulationRequest } from "@continuous-labs/sdk/models";

let value: RemoveWorldSimulationRequest = {};
```

## Fields

| Field                                                                                                                                                                 | Type                                                                                                                                                                  | Required                                                                                                                                                              | Description                                                                                                                                                           |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `delete`                                                                                                                                                              | *boolean*                                                                                                                                                             | :heavy_minus_sign:                                                                                                                                                    | true stops and deletes the member and its saved state. false, the default, detaches it: it keeps its ID, endpoint, token, clock, and data as a standalone Simulation. |