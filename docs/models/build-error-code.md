# BuildErrorCode

Stable build error code. live_credential_rejected is a build that waited at QA for its rejected live credentials and was not resumed within 7 days; live_rate_limited is one that waited at QA for the live systems' rate limit and was not resumed within 7 days.

## Example Usage

```typescript
import { BuildErrorCode } from "@continuous-labs/sdk/models";

let value: BuildErrorCode = "build_failed";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"build_failed" | "build_canceled" | "specification_validation_failed" | "live_credential_rejected" | "live_rate_limited" | Unrecognized<string>
```