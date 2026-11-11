# ListMcpboxSnapshotsRequest

## Example Usage

```typescript
import { ListMcpboxSnapshotsRequest } from "@continuous-labs/sdk/models/operations";

let value: ListMcpboxSnapshotsRequest = {};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `status`                                                                                        | [operations.ListMcpboxSnapshotsStatus](../../models/operations/list-mcpbox-snapshots-status.md) | :heavy_minus_sign:                                                                              | Optional build status filter.                                                                   |
| `limit`                                                                                         | *number*                                                                                        | :heavy_minus_sign:                                                                              | Page size. Values below 1 use 50. Values above 200 use 200.                                     |
| `cursor`                                                                                        | *string*                                                                                        | :heavy_minus_sign:                                                                              | Opaque next_cursor value from a previous page.                                                  |
| `source`                                                                                        | [operations.ListMcpboxSnapshotsSource](../../models/operations/list-mcpbox-snapshots-source.md) | :heavy_minus_sign:                                                                              | Optional source filter.                                                                         |
| `sourceBoxId`                                                                                   | *string*                                                                                        | :heavy_minus_sign:                                                                              | Optional filter for the Snapshots saved from this Box.                                          |