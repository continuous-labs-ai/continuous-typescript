# GetMCPBoxResponse

## Example Usage

```typescript
import { GetMCPBoxResponse } from "@continuous-labs/sdk/models";

let value: GetMCPBoxResponse = {
  apiboxId: "<id>",
  connection: {
    endpoint: "https://noteworthy-pepper.net/",
    token: "<value>",
  },
  createdAt: new Date("2024-07-24T18:52:49.535Z"),
  endpoint: "https://aggravating-junior.info",
  error: {
    code: "mcpbox_runtime_lost",
    detail: "<value>",
  },
  id: "<id>",
  lastActiveAt: new Date("2026-08-18T12:12:22.641Z"),
  metadata: "<value>",
  name: "<value>",
  snapshotId: "<id>",
  status: "stopping",
  statusChangedAt: new Date("2026-08-06T16:07:44.228Z"),
};
```

## Fields

| Field                                                                                                                                    | Type                                                                                                                                     | Required                                                                                                                                 | Description                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| `apiboxId`                                                                                                                               | *string*                                                                                                                                 | :heavy_check_mark:                                                                                                                       | The API Box it fronts, whose state its tools read and change.                                                                            |
| `connection`                                                                                                                             | [models.MCPBoxConnection](../models/mcp-box-connection.md)                                                                               | :heavy_check_mark:                                                                                                                       | The MCP Box's endpoint and token, or null while it has no stored token; its next start issues one.                                       |
| `createdAt`                                                                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                            | :heavy_check_mark:                                                                                                                       | MCP Box creation time.                                                                                                                   |
| `endpoint`                                                                                                                               | *string*                                                                                                                                 | :heavy_check_mark:                                                                                                                       | Base URL of the MCP Box. Send MCP Streamable HTTP requests to it followed by /mcp, with the MCP Box's token in X-Continuous-Token.       |
| `error`                                                                                                                                  | [models.BoxError](../models/box-error.md)                                                                                                | :heavy_check_mark:                                                                                                                       | N/A                                                                                                                                      |
| `id`                                                                                                                                     | *string*                                                                                                                                 | :heavy_check_mark:                                                                                                                       | MCP Box ID.                                                                                                                              |
| `lastActiveAt`                                                                                                                           | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                            | :heavy_check_mark:                                                                                                                       | Time of the Box's last data-plane activity.                                                                                              |
| `metadata`                                                                                                                               | *any*                                                                                                                                    | :heavy_check_mark:                                                                                                                       | Customer JSON metadata, or null.                                                                                                         |
| `name`                                                                                                                                   | *string*                                                                                                                                 | :heavy_check_mark:                                                                                                                       | MCP Box name. The ID is its identity, and names need not be unique.                                                                      |
| `snapshotId`                                                                                                                             | *string*                                                                                                                                 | :heavy_check_mark:                                                                                                                       | The MCP Box Snapshot it serves.                                                                                                          |
| `status`                                                                                                                                 | [models.GetMCPBoxResponseStatus](../models/get-mcp-box-response-status.md)                                                               | :heavy_check_mark:                                                                                                                       | starting while its runtime boots; running while it serves MCP; stopping while it releases its runtime; stopped when it holds no runtime. |
| `statusChangedAt`                                                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                            | :heavy_check_mark:                                                                                                                       | When the Box entered its current status, such as how long it has been starting.                                                          |