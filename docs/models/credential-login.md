# CredentialLogin

## Example Usage

```typescript
import { CredentialLogin } from "@continuous-labs/sdk/models";

let value: CredentialLogin = {
  hosts: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
  url: "https://decent-provision.biz",
  username: "Leonardo81",
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `hosts`                                                                                     | *string*[]                                                                                  | :heavy_check_mark:                                                                          | Further literal host names or IP addresses the app loads from, such as its API or CDN host. |
| `url`                                                                                       | *string*                                                                                    | :heavy_check_mark:                                                                          | The https URL of the app's sign-in page.                                                    |
| `username`                                                                                  | *string*                                                                                    | :heavy_check_mark:                                                                          | The user name to sign in with.                                                              |