# SnapshotComposition

## Example Usage

```typescript
import { SnapshotComposition } from "@continuous-labs/sdk/models";

let value: SnapshotComposition = {
  entities: 972088,
  operations: 381020,
  sample: true,
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `entities`                                                           | *number*                                                             | :heavy_check_mark:                                                   | Entities that the service stores.                                    |
| `operations`                                                         | *number*                                                             | :heavy_check_mark:                                                   | Operations that the service routes.                                  |
| `sample`                                                             | *boolean*                                                            | :heavy_check_mark:                                                   | Whether the build carries sample data that a new Box can start with. |