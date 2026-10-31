# McpboxTokenResponse

## Example Usage

```typescript
import { McpboxTokenResponse } from "@continuous-labs/sdk/models";

let value: McpboxTokenResponse = {
  mcpbox: {
    apiboxId: "<id>",
    createdAt: new Date("2025-08-29T11:19:18.928Z"),
    endpoint: "<value>",
    error: null,
    id: "<id>",
    metadata: "<value>",
    name: "<value>",
    snapshotId: "<id>",
    status: "stopped",
  },
  token: "<value>",
};
```

## Fields

| Field                                                                                                                                                            | Type                                                                                                                                                             | Required                                                                                                                                                         | Description                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `mcpbox`                                                                                                                                                         | [models.MCPBox](../models/mcp-box.md)                                                                                                                            | :heavy_check_mark:                                                                                                                                               | N/A                                                                                                                                                              |
| `token`                                                                                                                                                          | *string*                                                                                                                                                         | :heavy_check_mark:                                                                                                                                               | The MCP Box's token, which lasts until the MCP Box is deleted. It is null only on a retried create whose first attempt stored no token; a start then issues one. |