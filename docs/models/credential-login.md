# CredentialLogin

## Example Usage

```typescript
import { CredentialLogin } from "@continuous-labs/sdk/models";

let value: CredentialLogin = {
  signedInAt: new Date("2026-10-30T10:33:02.214Z"),
  url: "https://second-hand-exhaust.name/",
};
```

## Fields

| Field                                                                                                              | Type                                                                                                               | Required                                                                                                           | Description                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| `signedInAt`                                                                                                       | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                      | :heavy_check_mark:                                                                                                 | When a person last signed in by hand in the console, or null. A build cannot use a login before its first sign-in. |
| `url`                                                                                                              | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | The https URL of the app's sign-in page.                                                                           |