# CloneBoxSnapshotRequest

## Example Usage

```typescript
import { CloneBoxSnapshotRequest } from "@continuous-labs/sdk/models";

let value: CloneBoxSnapshotRequest = {
  targetWorkspaceId: "<id>",
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `name`                                                                       | *string*                                                                     | :heavy_minus_sign:                                                           | Name for the clone. Defaults to the source Snapshot's name.                  |
| `targetWorkspaceId`                                                          | *string*                                                                     | :heavy_check_mark:                                                           | Workspace that receives the clone. It must differ from the source workspace. |