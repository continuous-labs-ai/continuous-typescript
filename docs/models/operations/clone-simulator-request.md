# CloneSimulatorRequest

## Example Usage

```typescript
import { CloneSimulatorRequest } from "@continuous-labs/sdk/models/operations";

let value: CloneSimulatorRequest = {
  id: "<id>",
  body: {
    idempotencyKey: "<value>",
    targetWorkspaceId: "<id>",
  },
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `id`                                                                    | *string*                                                                | :heavy_check_mark:                                                      | Source Simulator ID.                                                    |
| `body`                                                                  | [models.CloneSimulatorRequest](../../models/clone-simulator-request.md) | :heavy_check_mark:                                                      | N/A                                                                     |