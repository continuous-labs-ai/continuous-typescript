# CreateWebBoxResponse

## Example Usage

```typescript
import { CreateWebBoxResponse } from "@continuous-labs/sdk/models";

let value: CreateWebBoxResponse = {
  webbox: {
    createdAt: new Date("2024-09-16T13:00:47.056Z"),
    deletedAt: new Date("2025-02-10T20:19:09.886Z"),
    error: {
      code: "mcpbox_apibox_unissued",
      detail: "<value>",
    },
    id: "<id>",
    includeSampleData: false,
    lastActiveAt: new Date("2026-02-28T23:04:19.639Z"),
    metadata: "<value>",
    name: "<value>",
    snapshotId: "<id>",
    status: "stopping",
    statusChangedAt: new Date("2026-01-08T17:00:18.009Z"),
    url: "https://acclaimed-jellyfish.name",
  },
};
```

## Fields

| Field                                 | Type                                  | Required                              | Description                           |
| ------------------------------------- | ------------------------------------- | ------------------------------------- | ------------------------------------- |
| `webbox`                              | [models.WebBox](../models/web-box.md) | :heavy_check_mark:                    | N/A                                   |