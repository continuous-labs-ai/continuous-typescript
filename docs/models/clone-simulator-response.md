# CloneSimulatorResponse

## Example Usage

```typescript
import { CloneSimulatorResponse } from "@continuous-labs/sdk/models";

let value: CloneSimulatorResponse = {
  digest: "<value>",
  id: "<id>",
  name: "<value>",
  workspaceId: "<id>",
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `digest`                                                                         | *string*                                                                         | :heavy_check_mark:                                                               | OCI manifest digest, unchanged from the source.                                  |
| `id`                                                                             | *string*                                                                         | :heavy_check_mark:                                                               | New Simulator ID in the target workspace, or the same ID on an idempotent retry. |
| `name`                                                                           | *string*                                                                         | :heavy_check_mark:                                                               | Display name of the clone.                                                       |
| `workspaceId`                                                                    | *string*                                                                         | :heavy_check_mark:                                                               | Target workspace.                                                                |