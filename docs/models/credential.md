# Credential

## Example Usage

```typescript
import { Credential } from "@continuous-labs/sdk/models";

let value: Credential = {
  baseUrl: "https://api.stripe.com",
  createdAt: new Date("2026-01-15T12:00:00Z"),
  header: "Authorization",
  id: "crd_01J8Z5X4K7M2N9P0Q1R2S3T4VA",
  name: "stripe-test",
};
```

## Fields

| Field                                                                                                                              | Type                                                                                                                               | Required                                                                                                                           | Description                                                                                                                        |
| ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `baseUrl`                                                                                                                          | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | The https URL of the real system, or null for a credential created without one. A build can use only a credential with a base URL. |
| `createdAt`                                                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                      | :heavy_check_mark:                                                                                                                 | Credential creation time.                                                                                                          |
| `header`                                                                                                                           | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | The HTTP header that carries the value.                                                                                            |
| `id`                                                                                                                               | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | Credential ID.                                                                                                                     |
| `name`                                                                                                                             | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | Credential name. Names need not be unique.                                                                                         |