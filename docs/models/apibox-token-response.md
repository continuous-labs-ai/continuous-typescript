# ApiboxTokenResponse

## Example Usage

```typescript
import { ApiboxTokenResponse } from "@continuous-labs/sdk/models";

let value: ApiboxTokenResponse = {
  apibox: {
    createdAt: new Date("2024-04-09T07:32:50.109Z"),
    endpoint: "<value>",
    error: {
      agentMessage: "<value>",
      code: "specification_validation_failed",
      detail: "<value>",
      reason: "specification_invalid",
      validation: {
        issues: [],
      },
    },
    id: "<id>",
    includeSampleData: true,
    metadata: "<value>",
    name: "<value>",
    snapshotId: "<id>",
    status: "starting",
  },
  token: "<value>",
};
```

## Fields

| Field                                                                                                                                                            | Type                                                                                                                                                             | Required                                                                                                                                                         | Description                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `apibox`                                                                                                                                                         | [models.APIBox](../models/api-box.md)                                                                                                                            | :heavy_check_mark:                                                                                                                                               | N/A                                                                                                                                                              |
| `token`                                                                                                                                                          | *string*                                                                                                                                                         | :heavy_check_mark:                                                                                                                                               | The API Box's token, which lasts until the API Box is deleted. It is null only on a retried create whose first attempt stored no token; a start then issues one. |