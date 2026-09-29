# CurrentSimulationToken

## Example Usage

```typescript
import { CurrentSimulationToken } from "@continuous-labs/sdk/models";

let value: CurrentSimulationToken = {
  expiresAt: null,
  token: "<redacted>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `expiresAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Null for a lifetime credential.                                                               |
| `token`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | Current Simulation endpoint credential.                                                       |