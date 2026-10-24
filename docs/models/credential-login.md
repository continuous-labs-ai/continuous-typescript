# CredentialLogin

## Example Usage

```typescript
import { CredentialLogin } from "@continuous-labs/sdk/models";

let value: CredentialLogin = {
  url: "https://watery-commodity.net",
  username: "Elody8",
};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `url`                                    | *string*                                 | :heavy_check_mark:                       | The https URL of the app's sign-in page. |
| `username`                               | *string*                                 | :heavy_check_mark:                       | The user name to sign in with.           |