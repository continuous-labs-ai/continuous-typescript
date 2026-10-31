# ListAPIBoxSnapshotsResponse

## Example Usage

```typescript
import { ListAPIBoxSnapshotsResponse } from "@continuous-labs/sdk/models";

let value: ListAPIBoxSnapshotsResponse = {
  nextCursor: "<value>",
  snapshots: [],
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `nextCursor`                                             | *string*                                                 | :heavy_check_mark:                                       | Cursor for the next page, or null.                       |
| `snapshots`                                              | [models.APIBoxSnapshot](../models/api-box-snapshot.md)[] | :heavy_check_mark:                                       | API Box Snapshots in this page.                          |