# ResourceError

## Example Usage

```typescript
import { ResourceError } from "@continuous-labs/sdk/models";

let value: ResourceError = {
  code: "<value>",
  detail: "<value>",
};
```

## Fields

| Field                               | Type                                | Required                            | Description                         |
| ----------------------------------- | ----------------------------------- | ----------------------------------- | ----------------------------------- |
| `code`                              | *string*                            | :heavy_check_mark:                  | Stable machine-readable error code. |
| `detail`                            | *string*                            | :heavy_check_mark:                  | Safe human-readable error detail.   |