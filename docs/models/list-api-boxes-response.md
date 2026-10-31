# ListAPIBoxesResponse

## Example Usage

```typescript
import { ListAPIBoxesResponse } from "@continuous-labs/sdk/models";

let value: ListAPIBoxesResponse = {
  apiboxes: [
    {
      createdAt: new Date("2024-03-17T19:39:51.908Z"),
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
      includeSampleData: false,
      metadata: "<value>",
      name: "<value>",
      snapshotId: "<id>",
      status: "stopped",
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