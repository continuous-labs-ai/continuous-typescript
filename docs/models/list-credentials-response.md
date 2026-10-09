# ListCredentialsResponse

## Example Usage

```typescript
import { ListCredentialsResponse } from "@continuous-labs/sdk/models";

let value: ListCredentialsResponse = {
  credentials: [
    {
      baseUrl: "https://api.stripe.com",
      createdAt: new Date("2026-01-15T12:00:00Z"),
      header: "Authorization",
      id: "crd_01J8Z5X4K7M2N9P0Q1R2S3T4VA",
      name: "stripe-test",
    },
  ],
  nextCursor: "<value>",
};
```

## Fields

| Field                                           | Type                                            | Required                                        | Description                                     |
| ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- |
| `credentials`                                   | [models.Credential](../models/credential.md)[]  | :heavy_check_mark:                              | Credential metadata in this page, newest first. |
| `nextCursor`                                    | *string*                                        | :heavy_check_mark:                              | Cursor for the next page, or null.              |