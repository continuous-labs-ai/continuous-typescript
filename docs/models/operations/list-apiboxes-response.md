# ListApiboxesResponse

## Example Usage

```typescript
import { ListApiboxesResponse } from "@continuous-labs/sdk/models/operations";

let value: ListApiboxesResponse = {
  result: {
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
  },
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `result`                                                               | [models.ListAPIBoxesResponse](../../models/list-api-boxes-response.md) | :heavy_check_mark:                                                     | N/A                                                                    |