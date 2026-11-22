# ListWebboxesRequest

## Example Usage

```typescript
import { ListWebboxesRequest } from "@continuous-labs/sdk/models/operations";

let value: ListWebboxesRequest = {};
```

## Fields

| Field                                                                                                              | Type                                                                                                               | Required                                                                                                           | Description                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| `status`                                                                                                           | [operations.ListWebboxesStatus](../../models/operations/list-webboxes-status.md)                                   | :heavy_minus_sign:                                                                                                 | Only Web Boxes with this status.                                                                                   |
| `snapshotId`                                                                                                       | *string*                                                                                                           | :heavy_minus_sign:                                                                                                 | Only Web Boxes started from this Snapshot.                                                                         |
| `limit`                                                                                                            | *number*                                                                                                           | :heavy_minus_sign:                                                                                                 | Page size. Values below 1 use 50. Values above 200 use 200.                                                        |
| `cursor`                                                                                                           | *string*                                                                                                           | :heavy_minus_sign:                                                                                                 | Opaque next_cursor value from a previous page.                                                                     |
| `deleted`                                                                                                          | *boolean*                                                                                                          | :heavy_minus_sign:                                                                                                 | List only the Web Boxes deleted in the last 14 days, each with when it was deleted, in place of those not deleted. |