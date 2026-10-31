# ListApiboxesRequest

## Example Usage

```typescript
import { ListApiboxesRequest } from "@continuous-labs/sdk/models/operations";

let value: ListApiboxesRequest = {};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `status`                                                                         | [operations.ListApiboxesStatus](../../models/operations/list-apiboxes-status.md) | :heavy_minus_sign:                                                               | Only API Boxes with this status.                                                 |
| `snapshotId`                                                                     | *string*                                                                         | :heavy_minus_sign:                                                               | Only API Boxes started from this Snapshot.                                       |
| `limit`                                                                          | *number*                                                                         | :heavy_minus_sign:                                                               | Page size. Values below 1 use 50. Values above 200 use 200.                      |
| `cursor`                                                                         | *string*                                                                         | :heavy_minus_sign:                                                               | Opaque next_cursor value from a previous page.                                   |