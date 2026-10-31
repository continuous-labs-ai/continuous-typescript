# ListMcpboxesRequest

## Example Usage

```typescript
import { ListMcpboxesRequest } from "@continuous-labs/sdk/models/operations";

let value: ListMcpboxesRequest = {};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `status`                                                                         | [operations.ListMcpboxesStatus](../../models/operations/list-mcpboxes-status.md) | :heavy_minus_sign:                                                               | Only MCP Boxes with this status.                                                 |
| `snapshotId`                                                                     | *string*                                                                         | :heavy_minus_sign:                                                               | Only MCP Boxes that serve this Snapshot.                                         |
| `limit`                                                                          | *number*                                                                         | :heavy_minus_sign:                                                               | Page size. Values below 1 use 50. Values above 200 use 200.                      |
| `cursor`                                                                         | *string*                                                                         | :heavy_minus_sign:                                                               | Opaque next_cursor value from a previous page.                                   |