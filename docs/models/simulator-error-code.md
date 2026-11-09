# SimulatorErrorCode

Stable Simulator build error code. live_credential_rejected is a build that waited at QA for its rejected live credentials and was not resumed within 7 days; live_rate_limited is one that waited at QA for the live systems' rate limit and was not resumed within 7 days.

## Example Usage

```typescript
import { SimulatorErrorCode } from "@continuous-labs/sdk/models";

let value: SimulatorErrorCode = "live_rate_limited";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"build_failed" | "build_canceled" | "specification_validation_failed" | "live_credential_rejected" | "live_rate_limited" | Unrecognized<string>
```