# MintSimulationTokenResponse

## Example Usage

```typescript
import { MintSimulationTokenResponse } from "@continuous-labs/sdk/models/operations";

let value: MintSimulationTokenResponse = {
  headers: {
    "key": [],
  },
  result: {
    expiresAt: null,
    token: "<redacted>",
  },
};
```

## Fields

| Field                                                                     | Type                                                                      | Required                                                                  | Description                                                               | Example                                                                   |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `headers`                                                                 | Record<string, *string*[]>                                                | :heavy_check_mark:                                                        | N/A                                                                       |                                                                           |
| `result`                                                                  | [models.CurrentSimulationToken](../../models/current-simulation-token.md) | :heavy_check_mark:                                                        | N/A                                                                       | {<br/>"expires_at": null,<br/>"token": "\u003credacted\u003e"<br/>}       |