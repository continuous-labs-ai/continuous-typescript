# ListMCPBoxesResponse

## Example Usage

```typescript
import { ListMCPBoxesResponse } from "@continuous-labs/sdk/models";

let value: ListMCPBoxesResponse = {
  mcpboxes: [
    {
      apiboxId: "<id>",
      createdAt: new Date("2024-05-06T22:20:10.955Z"),
      endpoint: "https://appropriate-stock.net",
      error: {
        code: "mcpbox_runtime_lost",
        detail: "<value>",
      },
      id: "<id>",
      lastActiveAt: new Date("2025-07-16T06:28:16.049Z"),
      metadata: "<value>",
      name: "<value>",
      snapshotId: "<id>",
      status: "stopped",
      statusChangedAt: new Date("2025-05-21T00:41:49.353Z"),
    },
  ],
  nextCursor: "<value>",
};
```

## Fields

| Field                                   | Type                                    | Required                                | Description                             |
| --------------------------------------- | --------------------------------------- | --------------------------------------- | --------------------------------------- |
| `mcpboxes`                              | [models.MCPBox](../models/mcp-box.md)[] | :heavy_check_mark:                      | MCP Boxes in this page.                 |
| `nextCursor`                            | *string*                                | :heavy_check_mark:                      | Cursor for the next page, or null.      |