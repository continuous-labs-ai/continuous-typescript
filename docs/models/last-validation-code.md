# LastValidationCode

Fixed code for the latest validation finding. Null when no finding is available. Authored details stay private.

## Example Usage

```typescript
import { LastValidationCode } from "@continuous-labs/sdk/models";

let value: LastValidationCode = "unsupported_claim";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"invalid_plan" | "unsupported_claim" | "invalid_requirement" | "nested_proof" | "request_not_satisfied" | "verification_unavailable" | Unrecognized<string>
```