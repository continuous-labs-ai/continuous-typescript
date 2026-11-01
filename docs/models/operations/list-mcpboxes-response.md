# ListMcpboxesResponse

## Example Usage

```typescript
import { ListMcpboxesResponse } from "@continuous-labs/sdk/models/operations";

let value: ListMcpboxesResponse = {
  result: {
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
  },
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `result`                                                               | [models.ListMCPBoxesResponse](../../models/list-mcp-boxes-response.md) | :heavy_check_mark:                                                     | N/A                                                                    |