# CreateCredentialRequest

## Example Usage

```typescript
import { CreateCredentialRequest } from "@continuous-labs/sdk/models";

let value: CreateCredentialRequest = {
  baseUrl: "https://api.stripe.com",
  name: "stripe-test",
  value: "Bearer <redacted>",
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `baseUrl`                                                                                | *string*                                                                                 | :heavy_check_mark:                                                                       | The https URL of the real system. Requests go to paths under it.                         |
| `header`                                                                                 | *string*                                                                                 | :heavy_minus_sign:                                                                       | The HTTP header that carries the value.                                                  |
| `name`                                                                                   | *string*                                                                                 | :heavy_check_mark:                                                                       | Credential name.                                                                         |
| `value`                                                                                  | *string*                                                                                 | :heavy_check_mark:                                                                       | The full header value, for example Bearer followed by a token. The API never returns it. |