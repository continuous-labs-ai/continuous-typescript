# RegenerateSimulationTokenResponse

## Example Usage

```typescript
import { RegenerateSimulationTokenResponse } from "@continuous-labs/sdk/models/operations";

let value: RegenerateSimulationTokenResponse = {
  headers: {
    "key": [
      "<value 1>",
    ],
    "key1": [
      "<value 1>",
    ],
    "key2": [],
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