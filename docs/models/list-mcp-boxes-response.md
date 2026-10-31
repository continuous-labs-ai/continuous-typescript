# ListMCPBoxesResponse

## Example Usage

```typescript
import { ListMCPBoxesResponse } from "@continuous-labs/sdk/models";

let value: ListMCPBoxesResponse = {
  mcpboxes: [
    {
      apiboxId: "<id>",
      createdAt: new Date("2024-05-06T22:20:10.955Z"),
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
      metadata: "<value>",
      name: "<value>",
      snapshotId: "<id>",
      status: "starting",
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