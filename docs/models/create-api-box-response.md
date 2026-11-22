# CreateAPIBoxResponse

## Example Usage

```typescript
import { CreateAPIBoxResponse } from "@continuous-labs/sdk/models";

let value: CreateAPIBoxResponse = {
  apibox: {
    createdAt: new Date("2026-10-19T23:42:15.600Z"),
    deletedAt: new Date("2026-09-03T23:04:53.868Z"),
    endpoint: "https://inexperienced-configuration.info",
    error: {
      code: "mcpbox_apibox_unissued",
      detail: "<value>",
    },
    id: "<id>",
    includeSampleData: true,
    lastActiveAt: new Date("2024-01-30T05:44:46.139Z"),
    metadata: "<value>",
    name: "<value>",
    snapshotId: "<id>",
    status: "stopping",
    statusChangedAt: new Date("2026-03-16T00:30:22.935Z"),
  },
  token: "<value>",
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `apibox`                                                       | [models.APIBox](../models/api-box.md)                          | :heavy_check_mark:                                             | N/A                                                            |
| `token`                                                        | *string*                                                       | :heavy_check_mark:                                             | The API Box's token, which lasts until the API Box is deleted. |