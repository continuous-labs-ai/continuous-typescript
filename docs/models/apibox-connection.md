# ApiboxConnection

## Example Usage

```typescript
import { ApiboxConnection } from "@continuous-labs/sdk/models";

let value: ApiboxConnection = {
  endpoint: "<value>",
  token: "<value>",
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `endpoint`                                                                          | *string*                                                                            | :heavy_check_mark:                                                                  | Base URL of the API Box's API.                                                      |
| `token`                                                                             | *string*                                                                            | :heavy_check_mark:                                                                  | The API Box's token. Send it in X-Continuous-Token on each request to the endpoint. |