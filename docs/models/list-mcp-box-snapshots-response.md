# ListMCPBoxSnapshotsResponse

## Example Usage

```typescript
import { ListMCPBoxSnapshotsResponse } from "@continuous-labs/sdk/models";

let value: ListMCPBoxSnapshotsResponse = {
  nextCursor: "<value>",
  snapshots: [],
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `nextCursor`                                             | *string*                                                 | :heavy_check_mark:                                       | Cursor for the next page, or null.                       |
| `snapshots`                                              | [models.MCPBoxSnapshot](../models/mcp-box-snapshot.md)[] | :heavy_check_mark:                                       | MCP Box Snapshots in this page.                          |