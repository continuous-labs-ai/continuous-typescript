# CreateCredentialRequest

## Example Usage

```typescript
import { CreateCredentialRequest } from "@continuous-labs/sdk/models";

let value: CreateCredentialRequest = {
  baseUrl: "https://api.stripe.com",
  header: "Authorization",
  name: "stripe-test",
  value: "Bearer <redacted>",
};
```

## Fields

| Field                                                                                                           | Type                                                                                                            | Required                                                                                                        | Description                                                                                                     |
| --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| `baseUrl`                                                                                                       | *string*                                                                                                        | :heavy_minus_sign:                                                                                              | The https URL of the real system. Requests go to paths under it. Send exactly one of base_url and login.        |
| `header`                                                                                                        | *string*                                                                                                        | :heavy_minus_sign:                                                                                              | The HTTP header that carries the value. Defaults to Authorization. Not allowed with login.                      |
| `login`                                                                                                         | [models.CredentialLoginRequest](../models/credential-login-request.md)                                          | :heavy_minus_sign:                                                                                              | N/A                                                                                                             |
| `name`                                                                                                          | *string*                                                                                                        | :heavy_check_mark:                                                                                              | Credential name.                                                                                                |
| `value`                                                                                                         | *string*                                                                                                        | :heavy_check_mark:                                                                                              | The full header value, for example Bearer followed by a token, or the login password. The API never returns it. |