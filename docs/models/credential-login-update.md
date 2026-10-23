# CredentialLoginUpdate

## Example Usage

```typescript
import { CredentialLoginUpdate } from "@continuous-labs/sdk/models";

let value: CredentialLoginUpdate = {
  hosts: [],
};
```

## Fields

| Field                                                                                                                 | Type                                                                                                                  | Required                                                                                                              | Description                                                                                                           |
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `hosts`                                                                                                               | *string*[]                                                                                                            | :heavy_check_mark:                                                                                                    | The full list of further hosts the app loads from, which replaces the current list. Send the current list to keep it. |
| `url`                                                                                                                 | *string*                                                                                                              | :heavy_minus_sign:                                                                                                    | New https URL of the app's sign-in page.                                                                              |
| `username`                                                                                                            | *string*                                                                                                              | :heavy_minus_sign:                                                                                                    | New user name.                                                                                                        |