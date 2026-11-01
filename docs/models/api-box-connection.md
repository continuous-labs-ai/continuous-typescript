# APIBoxConnection

## Example Usage

```typescript
import { APIBoxConnection } from "@continuous-labs/sdk/models";

let value: APIBoxConnection = {
  endpoint: "https://ambitious-eggplant.info/",
  token: "<value>",
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `endpoint`                                                                          | *string*                                                                            | :heavy_check_mark:                                                                  | Base URL of the API Box's API.                                                      |
| `token`                                                                             | *string*                                                                            | :heavy_check_mark:                                                                  | The API Box's token. Send it in X-Continuous-Token on each request to the endpoint. |