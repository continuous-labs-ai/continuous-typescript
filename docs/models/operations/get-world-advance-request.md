# GetWorldAdvanceRequest

## Example Usage

```typescript
import { GetWorldAdvanceRequest } from "@continuous-labs/sdk/models/operations";

let value: GetWorldAdvanceRequest = {
  id: "<id>",
  advanceId: "<id>",
};
```

## Fields

| Field                       | Type                        | Required                    | Description                 |
| --------------------------- | --------------------------- | --------------------------- | --------------------------- |
| `id`                        | *string*                    | :heavy_check_mark:          | Simulation or World ID.     |
| `advanceId`                 | *string*                    | :heavy_check_mark:          | Clock advance operation ID. |