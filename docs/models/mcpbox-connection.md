# McpboxConnection

## Example Usage

```typescript
import { McpboxConnection } from "@continuous-labs/sdk/models";

let value: McpboxConnection = {
  endpoint: "<value>",
  token: "<value>",
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `endpoint`                                                              | *string*                                                                | :heavy_check_mark:                                                      | Base URL of the MCP Box; its MCP endpoint is this URL followed by /mcp. |
| `token`                                                                 | *string*                                                                | :heavy_check_mark:                                                      | The MCP Box's token. Send it in X-Continuous-Token on each request.     |