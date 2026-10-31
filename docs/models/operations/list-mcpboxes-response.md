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
  },
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `result`                                                               | [models.ListMCPBoxesResponse](../../models/list-mcp-boxes-response.md) | :heavy_check_mark:                                                     | N/A                                                                    |