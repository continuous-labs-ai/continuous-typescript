# ListApiboxSnapshotsRequest

## Example Usage

```typescript
import { ListApiboxSnapshotsRequest } from "@continuous-labs/sdk/models/operations";

let value: ListApiboxSnapshotsRequest = {};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `status`                                                                                        | [operations.ListApiboxSnapshotsStatus](../../models/operations/list-apibox-snapshots-status.md) | :heavy_minus_sign:                                                                              | Optional build status filter.                                                                   |
| `limit`                                                                                         | *number*                                                                                        | :heavy_minus_sign:                                                                              | Page size. Values below 1 use 50. Values above 200 use 200.                                     |
| `cursor`                                                                                        | *string*                                                                                        | :heavy_minus_sign:                                                                              | Opaque next_cursor value from a previous page.                                                  |
| `source`                                                                                        | [operations.ListApiboxSnapshotsSource](../../models/operations/list-apibox-snapshots-source.md) | :heavy_minus_sign:                                                                              | Optional source filter.                                                                         |