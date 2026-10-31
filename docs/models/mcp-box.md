# MCPBox

## Example Usage

```typescript
import { MCPBox } from "@continuous-labs/sdk/models";

let value: MCPBox = {
  apiboxId: "<id>",
  createdAt: new Date("2025-11-05T15:54:36.281Z"),
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
  status: "stopping",
};
```

## Fields

| Field                                                                                                                                    | Type                                                                                                                                     | Required                                                                                                                                 | Description                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| `apiboxId`                                                                                                                               | *string*                                                                                                                                 | :heavy_check_mark:                                                                                                                       | The API Box it fronts, whose state its tools read and change.                                                                            |
| `createdAt`                                                                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                            | :heavy_check_mark:                                                                                                                       | MCP Box creation time.                                                                                                                   |
| `endpoint`                                                                                                                               | *string*                                                                                                                                 | :heavy_check_mark:                                                                                                                       | Base URL of the MCP Box. Send MCP Streamable HTTP requests to it followed by /mcp, with the MCP Box's token in X-Continuous-Token.       |
| `error`                                                                                                                                  | [models.SimulatorError](../models/simulator-error.md)                                                                                    | :heavy_check_mark:                                                                                                                       | N/A                                                                                                                                      |
| `id`                                                                                                                                     | *string*                                                                                                                                 | :heavy_check_mark:                                                                                                                       | MCP Box ID.                                                                                                                              |
| `metadata`                                                                                                                               | *any*                                                                                                                                    | :heavy_check_mark:                                                                                                                       | Customer JSON metadata, or null.                                                                                                         |
| `name`                                                                                                                                   | *string*                                                                                                                                 | :heavy_check_mark:                                                                                                                       | MCP Box name. The ID is its identity, and names need not be unique.                                                                      |
| `snapshotId`                                                                                                                             | *string*                                                                                                                                 | :heavy_check_mark:                                                                                                                       | The MCP Box Snapshot it serves.                                                                                                          |
| `status`                                                                                                                                 | [models.MCPBoxStatus](../models/mcp-box-status.md)                                                                                       | :heavy_check_mark:                                                                                                                       | starting while its runtime boots; running while it serves MCP; stopping while it releases its runtime; stopped when it holds no runtime. |