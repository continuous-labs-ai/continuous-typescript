# CreateMCPBoxResponse

## Example Usage

```typescript
import { CreateMCPBoxResponse } from "@continuous-labs/sdk/models";

let value: CreateMCPBoxResponse = {
  mcpbox: {
    apiboxId: "<id>",
    createdAt: new Date("2024-12-09T09:21:40.748Z"),
    endpoint: "https://second-tenement.info/",
    error: null,
    id: "<id>",
    lastActiveAt: new Date("2026-02-21T02:28:04.168Z"),
    metadata: "<value>",
    name: "<value>",
    snapshotId: "<id>",
    status: "running",
    statusChangedAt: new Date("2026-09-21T20:34:19.859Z"),
  },
  token: null,
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `mcpbox`                                                       | [models.MCPBox](../models/mcp-box.md)                          | :heavy_check_mark:                                             | N/A                                                            |
| `token`                                                        | *string*                                                       | :heavy_check_mark:                                             | The MCP Box's token, which lasts until the MCP Box is deleted. |