# ListCredentialsResponse

## Example Usage

```typescript
import { ListCredentialsResponse } from "@continuous-labs/sdk/models/operations";

let value: ListCredentialsResponse = {
  result: {
    credentials: [
      {
        baseUrl: "https://api.stripe.com",
        createdAt: new Date("2026-01-15T12:00:00Z"),
        header: "Authorization",
        id: "crd_01J8Z5X4K7M2N9P0Q1R2S3T4VA",
        login: null,
        name: "stripe-test",
        oauth: null,
      },
    ],
    nextCursor: "<value>",
  },
};
```

## Fields

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `result`                                                                    | [models.ListCredentialsResponse](../../models/list-credentials-response.md) | :heavy_check_mark:                                                          | N/A                                                                         |