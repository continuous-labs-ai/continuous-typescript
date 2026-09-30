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

| Field                                                                                                                                                                                               | Type                                                                                                                                                                                                | Required                                                                                                                                                                                            | Description                                                                                                                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ~~`expiresAt`~~                                                                                                                                                                                     | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                                                       | :heavy_check_mark:                                                                                                                                                                                  | : warning: ** DEPRECATED **: This will be removed in a future release, please migrate away from it as soon as possible.<br/><br/>Always null; Simulation tokens do not expire. Deprecated; will be removed. |
| `token`                                                                                                                                                                                             | *string*                                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                                  | The Simulation's current token for requests to its endpoint. Send it in the X-Continuous-Simulation-Token header.                                                                                   |