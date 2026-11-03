# APIBoxTokenResponse

## Example Usage

```typescript
import { APIBoxTokenResponse } from "@continuous-labs/sdk/models";

let value: APIBoxTokenResponse = {
  apibox: {
    createdAt: new Date("2025-04-16T19:56:45.068Z"),
    endpoint: "https://personal-sandbar.info/",
    error: {
      code: "mcpbox_runtime_lost",
      detail: "<value>",
    },
    id: "<id>",
    includeSampleData: false,
    lastActiveAt: new Date("2024-05-31T04:30:02.669Z"),
    metadata: "<value>",
    name: "<value>",
    snapshotId: "<id>",
    status: "starting",
    statusChangedAt: new Date("2026-07-07T08:45:45.858Z"),
  },
  token: "<value>",
};
```

## Fields

| Field                                                                                                                              | Type                                                                                                                               | Required                                                                                                                           | Description                                                                                                                        |
| ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `apibox`                                                                                                                           | [models.APIBox](../models/api-box.md)                                                                                              | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `token`                                                                                                                            | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | The API Box's token, which lasts until the API Box is deleted. It is null only for a box created before boxes stored their tokens. |