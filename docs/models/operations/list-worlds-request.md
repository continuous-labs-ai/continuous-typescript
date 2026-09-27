# ListWorldsRequest

## Example Usage

```typescript
import { ListWorldsRequest } from "@continuous-labs/sdk/models/operations";

let value: ListWorldsRequest = {};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `status`                                                                     | [operations.ListWorldsStatus](../../models/operations/list-worlds-status.md) | :heavy_minus_sign:                                                           | Optional status filter.                                                      |
| `limit`                                                                      | *number*                                                                     | :heavy_minus_sign:                                                           | Page size. Values below 1 use 50. Values above 200 use 200.                  |
| `cursor`                                                                     | *string*                                                                     | :heavy_minus_sign:                                                           | Opaque next_cursor value from a previous page.                               |