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
          code: "mcpbox_runtime_lost",
          detail: "<value>",
        },
        id: "<id>",
        includeSampleData: false,
        lastActiveAt: new Date("2024-02-19T18:06:33.613Z"),
        metadata: "<value>",
        name: "<value>",
        snapshotId: "<id>",
        status: "stopping",
        statusChangedAt: new Date("2025-10-15T02:06:40.362Z"),
        url: "https://sardonic-skeleton.org",
      },
    ],
  },
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `result`                                                               | [models.ListWebBoxesResponse](../../models/list-web-boxes-response.md) | :heavy_check_mark:                                                     | N/A                                                                    |