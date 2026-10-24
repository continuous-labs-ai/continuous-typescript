# CredentialLoginRequest

## Example Usage

```typescript
import { CredentialLoginRequest } from "@continuous-labs/sdk/models";

let value: CredentialLoginRequest = {
  url: "https://numb-legislature.name/",
  username: "Abbie_Hahn-Schaden26",
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `url`                                                                                                    | *string*                                                                                                 | :heavy_check_mark:                                                                                       | The https URL of the app's sign-in page, with a literal host name or IP address and no user information. |
| `username`                                                                                               | *string*                                                                                                 | :heavy_check_mark:                                                                                       | The user name to sign in with.                                                                           |