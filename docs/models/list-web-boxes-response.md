# ListWebBoxesResponse

## Example Usage

```typescript
import { ListWebBoxesResponse } from "@continuous-labs/sdk/models";

let value: ListWebBoxesResponse = {
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
};
```

## Fields

| Field                                   | Type                                    | Required                                | Description                             |
| --------------------------------------- | --------------------------------------- | --------------------------------------- | --------------------------------------- |
| `nextCursor`                            | *string*                                | :heavy_check_mark:                      | Cursor for the next page, or null.      |
| `webboxes`                              | [models.WebBox](../models/web-box.md)[] | :heavy_check_mark:                      | Web Boxes in this page.                 |