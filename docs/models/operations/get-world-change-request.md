# GetWorldChangeRequest

## Example Usage

```typescript
import { GetWorldChangeRequest } from "@continuous-labs/sdk/models/operations";

let value: GetWorldChangeRequest = {
  id: "<id>",
  changeId: "<id>",
};
```

## Fields

| Field                 | Type                  | Required              | Description           |
| --------------------- | --------------------- | --------------------- | --------------------- |
| `id`                  | *string*              | :heavy_check_mark:    | World ID.             |
| `changeId`            | *string*              | :heavy_check_mark:    | Membership change ID. |