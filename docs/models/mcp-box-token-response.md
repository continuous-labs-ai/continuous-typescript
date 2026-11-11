# MCPBoxTokenResponse

## Example Usage

```typescript
import { MCPBoxTokenResponse } from "@continuous-labs/sdk/models";

let value: MCPBoxTokenResponse = {
  mcpbox: {
    apiboxId: "<id>",
    createdAt: new Date("2025-10-30T18:58:03.595Z"),
    endpoint: "https://fruitful-backbone.name",
    error: {
      code: "mcpbox_runtime_lost",
      detail: "<value>",
    },
    id: "<id>",
    lastActiveAt: new Date("2025-09-14T13:21:45.072Z"),
    metadata: "<value>",
    name: "<value>",
    snapshotId: "<id>",
    status: "starting",
    statusChangedAt: new Date("2026-04-28T11:13:05.008Z"),
  },
  token: "<value>",
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `mcpbox`                                                       | [models.MCPBox](../models/mcp-box.md)                          | :heavy_check_mark:                                             | N/A                                                            |
| `token`                                                        | *string*                                                       | :heavy_check_mark:                                             | The MCP Box's token, which lasts until the MCP Box is deleted. |