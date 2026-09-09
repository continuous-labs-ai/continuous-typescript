# MintSimulationTokenRequest

## Example Usage

```typescript
import { MintSimulationTokenRequest } from "@continuous-labs/sdk/models";

let value: MintSimulationTokenRequest = {
  ttlSeconds: 3600,
};
```

## Fields

| Field                                              | Type                                               | Required                                           | Description                                        |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `ttlSeconds`                                       | *number*                                           | :heavy_check_mark:                                 | Token lifetime in seconds, from 60 through 86,400. |