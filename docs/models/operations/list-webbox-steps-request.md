# ListWebboxStepsRequest

## Example Usage

```typescript
import { ListWebboxStepsRequest } from "@continuous-labs/sdk/models/operations";

let value: ListWebboxStepsRequest = {
  id: "<id>",
};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `id`                                                        | *string*                                                    | :heavy_check_mark:                                          | Web Box ID.                                                 |
| `cursor`                                                    | *string*                                                    | :heavy_minus_sign:                                          | Opaque next_cursor value from a previous page.              |
| `limit`                                                     | *number*                                                    | :heavy_minus_sign:                                          | Page size. Values below 1 use 50. Values above 200 use 200. |