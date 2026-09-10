# MintSimulationTokenRequest

## Example Usage

```typescript
import { MintSimulationTokenRequest } from "@continuous-labs/sdk/models/operations";

let value: MintSimulationTokenRequest = {
  id: "<id>",
  body: {
    ttlSeconds: 3600,
  },
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        | Example                                                                            |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `id`                                                                               | *string*                                                                           | :heavy_check_mark:                                                                 | Simulation ID.                                                                     |                                                                                    |
| `body`                                                                             | [models.MintSimulationTokenRequest](../../models/mint-simulation-token-request.md) | :heavy_check_mark:                                                                 | N/A                                                                                | {<br/>"ttl_seconds": 3600<br/>}                                                    |