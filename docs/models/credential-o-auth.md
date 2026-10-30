# CredentialOAuth

## Example Usage

```typescript
import { CredentialOAuth } from "@continuous-labs/sdk/models";

let value: CredentialOAuth = {
  algorithm: "<value>",
  authMethod: "client_secret",
  clientId: "<id>",
  keyId: "<id>",
  scope: "<value>",
  tokenUrl: "https://warlike-slide.org",
};
```

## Fields

| Field                                                                                                         | Type                                                                                                          | Required                                                                                                      | Description                                                                                                   |
| ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| `algorithm`                                                                                                   | *string*                                                                                                      | :heavy_check_mark:                                                                                            | The JWS algorithm of a private_key_jwt client's assertion, or empty.                                          |
| `authMethod`                                                                                                  | [models.AuthMethod](../models/auth-method.md)                                                                 | :heavy_check_mark:                                                                                            | How the client authenticates: client_secret, or private_key_jwt, a JWT assertion signed with its private key. |
| `clientId`                                                                                                    | *string*                                                                                                      | :heavy_check_mark:                                                                                            | The OAuth 2.0 client ID.                                                                                      |
| `keyId`                                                                                                       | *string*                                                                                                      | :heavy_check_mark:                                                                                            | The kid of a private_key_jwt client's key, such as a NetSuite certificate ID, or empty.                       |
| `scope`                                                                                                       | *string*                                                                                                      | :heavy_check_mark:                                                                                            | The space-separated scopes the token is requested with, or empty for the client's default.                    |
| `tokenUrl`                                                                                                    | *string*                                                                                                      | :heavy_check_mark:                                                                                            | The https URL of the OAuth 2.0 token endpoint.                                                                |