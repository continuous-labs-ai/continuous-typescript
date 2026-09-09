# ForkSimulationRequest

## Example Usage

```typescript
import { ForkSimulationRequest } from "@continuous-labs/sdk/models";

let value: ForkSimulationRequest = {
  atStep: 42,
  name: "billing-fork",
};
```

## Fields

| Field                                                              | Type                                                               | Required                                                           | Description                                                        |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `atStep`                                                           | *number*                                                           | :heavy_minus_sign:                                                 | Completed step to fork from. Omission forks from the latest state. |
| `name`                                                             | *string*                                                           | :heavy_minus_sign:                                                 | Optional child Simulation name. Omission generates a name.         |