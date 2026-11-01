# CreateWebBoxResponse

## Example Usage

```typescript
import { CreateWebBoxResponse } from "@continuous-labs/sdk/models";

let value: CreateWebBoxResponse = {
  webbox: {
    createdAt: new Date("2024-09-16T13:00:47.056Z"),
    error: {
      code: "mcpbox_runtime_lost",
      detail: "<value>",
    },
    id: "<id>",
    includeSampleData: true,
    lastActiveAt: new Date("2025-07-08T15:30:57.365Z"),
    metadata: "<value>",
    name: "<value>",
    snapshotId: "<id>",
    status: "stopping",
    statusChangedAt: new Date("2026-02-28T23:04:19.639Z"),
    url: "https://reflecting-publicity.com",
  },
};
```

## Fields

| Field                                 | Type                                  | Required                              | Description                           |
| ------------------------------------- | ------------------------------------- | ------------------------------------- | ------------------------------------- |
| `webbox`                              | [models.WebBox](../models/web-box.md) | :heavy_check_mark:                    | N/A                                   |