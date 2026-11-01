# ListAPIBoxesResponse

## Example Usage

```typescript
import { ListAPIBoxesResponse } from "@continuous-labs/sdk/models";

let value: ListAPIBoxesResponse = {
  apiboxes: [
    {
      createdAt: new Date("2024-03-17T19:39:51.908Z"),
      endpoint: "https://squeaky-onset.biz/",
      error: {
        code: "mcpbox_runtime_lost",
        detail: "<value>",
      },
      id: "<id>",
      includeSampleData: true,
      lastActiveAt: new Date("2026-09-01T00:10:59.574Z"),
      metadata: "<value>",
      name: "<value>",
      snapshotId: "<id>",
      status: "stopped",
      statusChangedAt: new Date("2024-11-18T03:55:14.254Z"),
    },
  ],
  nextCursor: "<value>",
};
```

## Fields

| Field                                   | Type                                    | Required                                | Description                             |
| --------------------------------------- | --------------------------------------- | --------------------------------------- | --------------------------------------- |
| `apiboxes`                              | [models.APIBox](../models/api-box.md)[] | :heavy_check_mark:                      | API Boxes in this page.                 |
| `nextCursor`                            | *string*                                | :heavy_check_mark:                      | Cursor for the next page, or null.      |