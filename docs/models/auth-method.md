# AuthMethod

How the client authenticates: client_secret, or private_key_jwt, a JWT assertion signed with its private key.

## Example Usage

```typescript
import { AuthMethod } from "@continuous-labs/sdk/models";

let value: AuthMethod = "private_key_jwt";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"client_secret" | "private_key_jwt" | Unrecognized<string>
```