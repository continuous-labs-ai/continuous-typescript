# Actor

## Example Usage

```typescript
import { Actor } from "@continuous-labs/sdk/models";

let value: Actor = {
  default: true,
  entity: "<value>",
  id: "<id>",
  name: "<value>",
  role: "<value>",
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `default`                                                                                           | *boolean*                                                                                           | :heavy_check_mark:                                                                                  | Whether a request without the header acts as this caller.                                           |
| `entity`                                                                                            | *string*                                                                                            | :heavy_check_mark:                                                                                  | The entity whose row the id keys.                                                                   |
| `id`                                                                                                | *string*                                                                                            | :heavy_check_mark:                                                                                  | The value to send in the X-Continuous-Actor header: the key of the identity row the caller acts as. |
| `name`                                                                                              | *string*                                                                                            | :heavy_check_mark:                                                                                  | The build's name for the caller.                                                                    |
| `role`                                                                                              | *string*                                                                                            | :heavy_check_mark:                                                                                  | The caller's role in the simulated service.                                                         |