# CloneSimulatorRequest

## Example Usage

```typescript
import { CloneSimulatorRequest } from "@continuous-labs/sdk/models";

let value: CloneSimulatorRequest = {
  idempotencyKey: "<value>",
  targetWorkspaceId: "<id>",
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `idempotencyKey`                                                             | *string*                                                                     | :heavy_check_mark:                                                           | Stable key for retrying this clone into the target workspace.                |
| `name`                                                                       | *string*                                                                     | :heavy_minus_sign:                                                           | Display name for the clone. Defaults to the source Simulator's name.         |
| `targetWorkspaceId`                                                          | *string*                                                                     | :heavy_check_mark:                                                           | Workspace that receives the clone. It must differ from the source workspace. |