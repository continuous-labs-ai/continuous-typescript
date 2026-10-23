# CredentialLoginRequest

## Example Usage

```typescript
import { CredentialLoginRequest } from "@continuous-labs/sdk/models";

let value: CredentialLoginRequest = {
  hosts: [
    "<value 1>",
  ],
  url: "https://miserly-lotion.com",
  username: "Walter_Schaden26",
};
```

## Fields

| Field                                                                                                                    | Type                                                                                                                     | Required                                                                                                                 | Description                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| `hosts`                                                                                                                  | *string*[]                                                                                                               | :heavy_check_mark:                                                                                                       | Further literal host names or IP addresses the app loads from, such as its API or CDN host. Send an empty list for none. |
| `url`                                                                                                                    | *string*                                                                                                                 | :heavy_check_mark:                                                                                                       | The https URL of the app's sign-in page, with a literal host name or IP address and no user information.                 |
| `username`                                                                                                               | *string*                                                                                                                 | :heavy_check_mark:                                                                                                       | The user name to sign in with.                                                                                           |