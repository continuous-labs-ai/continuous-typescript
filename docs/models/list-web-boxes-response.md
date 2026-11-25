# ListWebBoxesResponse

## Example Usage

```typescript
import { ListWebBoxesResponse } from "@continuous-labs/sdk/models";

let value: ListWebBoxesResponse = {
  nextCursor: "<value>",
  webboxes: [
    {
      apiboxId: "<id>",
      createdAt: new Date("2025-02-16T09:36:15.303Z"),
      deletedAt: new Date("2025-08-13T01:18:55.801Z"),
      error: null,
      id: "<id>",
      includeSampleData: false,
      lastActiveAt: new Date("2025-10-15T02:06:40.362Z"),
      metadata: "<value>",
      name: "<value>",
      snapshotId: "<id>",
      status: "stopped",
      statusChangedAt: new Date("2026-02-14T09:59:51.289Z"),
      url: "https://unlucky-co-producer.org",
    },
  ],
};
```

## Fields

| Field                                   | Type                                    | Required                                | Description                             |
| --------------------------------------- | --------------------------------------- | --------------------------------------- | --------------------------------------- |
| `nextCursor`                            | *string*                                | :heavy_check_mark:                      | Cursor for the next page, or null.      |
| `webboxes`                              | [models.WebBox](../models/web-box.md)[] | :heavy_check_mark:                      | Web Boxes in this page.                 |