# CreateMCPBoxResponse

## Example Usage

```typescript
import { CreateMCPBoxResponse } from "@continuous-labs/sdk/models";

let value: CreateMCPBoxResponse = {
  mcpbox: {
    apiboxId: "<id>",
    createdAt: new Date("2024-12-09T09:21:40.748Z"),
    deletedAt: new Date("2026-02-23T04:47:13.793Z"),
    endpoint: "https://ironclad-ad.net",
    error: {
      code: "mcpbox_apibox_unissued",
      detail: "<value>",
    },
    id: "<id>",
    lastActiveAt: new Date("2026-09-21T20:34:19.859Z"),
    metadata: "<value>",
    name: "<value>",
    snapshotId: "<id>",
    status: "starting",
    statusChangedAt: new Date("2025-07-12T05:23:06.065Z"),
  },
  token: "<value>",
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `mcpbox`                                                       | [models.MCPBox](../models/mcp-box.md)                          | :heavy_check_mark:                                             | N/A                                                            |
| `token`                                                        | *string*                                                       | :heavy_check_mark:                                             | The MCP Box's token, which lasts until the MCP Box is deleted. |