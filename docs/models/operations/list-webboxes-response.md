# ListWebboxesResponse

## Example Usage

```typescript
import { ListWebboxesResponse } from "@continuous-labs/sdk/models/operations";

let value: ListWebboxesResponse = {
  result: {
    nextCursor: "<value>",
    webboxes: [
      {
        createdAt: new Date("2025-02-16T09:36:15.303Z"),
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
        status: "starting",
        url: "https://parched-tectonics.net",
      },
    ],
  },
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `result`                                                               | [models.ListWebBoxesResponse](../../models/list-web-boxes-response.md) | :heavy_check_mark:                                                     | N/A                                                                    |