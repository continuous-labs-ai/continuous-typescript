# ListCredentialsRequest

## Example Usage

```typescript
import { ListCredentialsRequest } from "@continuous-labs/sdk/models/operations";

let value: ListCredentialsRequest = {};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `limit`                                                     | *number*                                                    | :heavy_minus_sign:                                          | Page size. Values below 1 use 50. Values above 200 use 200. |
| `cursor`                                                    | *string*                                                    | :heavy_minus_sign:                                          | Opaque next_cursor value from a previous page.              |