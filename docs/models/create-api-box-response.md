# CreateAPIBoxResponse

## Example Usage

```typescript
import { CreateAPIBoxResponse } from "@continuous-labs/sdk/models";

let value: CreateAPIBoxResponse = {
  apibox: {
    createdAt: new Date("2026-10-19T23:42:15.600Z"),
    endpoint: "https://unique-stool.info",
    error: {
      code: "mcpbox_runtime_lost",
      detail: "<value>",
    },
    id: "<id>",
    includeSampleData: true,
    lastActiveAt: new Date("2025-04-11T22:39:48.214Z"),
    metadata: "<value>",
    name: "<value>",
    snapshotId: "<id>",
    status: "starting",
    statusChangedAt: new Date("2024-01-30T05:44:46.139Z"),
  },
  token: "<value>",
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `apibox`                                                       | [models.APIBox](../models/api-box.md)                          | :heavy_check_mark:                                             | N/A                                                            |
| `token`                                                        | *string*                                                       | :heavy_check_mark:                                             | The API Box's token, which lasts until the API Box is deleted. |